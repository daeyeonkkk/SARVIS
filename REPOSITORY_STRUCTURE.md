# SARVIS Repository Structure

이 문서는 공개용 저장소에서 원본 소스의 폴더명과 파일명만 확인할 수 있도록 만든 구조 인벤토리입니다.
내부 구현, 설정값, 비공개 데이터, 실행 가능한 소스 내용은 공개하지 않기 위해 의도적으로 비워두었습니다.

## 생성 기준

- 원본 기준: SSAFY 원본 저장소의 Git tracked files
- 생성 시각: 2026-06-04 17:39:34 +09:00
- 원본 Git tracked file 수: 343
- 공개 repo의 각 skeleton 파일은 파일명을 보존하기 위한 0바이트 placeholder입니다.
- 루트 `README.md`와 이 문서는 공개 설명을 위해 내용을 유지합니다.

## 전체 구조

```text
.
+-- .gitignore
+-- .vscode
|   \-- settings.json
+-- BACKEND
|   \-- djangopjt
|       +-- .env.example
|       +-- .gitignore
|       +-- accounts
|       |   +-- __init__.py
|       |   +-- admin.py
|       |   +-- app_consumer.py
|       |   +-- apps.py
|       |   +-- auth_utils.py
|       |   +-- consumers.py
|       |   +-- decorators.py
|       |   +-- management
|       |   |   +-- __init__.py
|       |   |   \-- commands
|       |   |       \-- __init__.py
|       |   +-- migrations
|       |   |   +-- __init__.py
|       |   |   \-- 0001_initial.py
|       |   +-- models.py
|       |   +-- robot_arm.py
|       |   +-- routing.py
|       |   +-- serializers.py
|       |   +-- tasks.py
|       |   +-- tests.py
|       |   +-- urls.py
|       |   +-- views.py
|       |   \-- websocket_logger.py
|       +-- gms_proxy
|       |   +-- .gitignore
|       |   \-- app.py
|       +-- manage.py
|       +-- requirements.txt
|       \-- server
|           +-- __init__.py
|           +-- asgi.py
|           +-- celery.py
|           +-- consumers.py
|           +-- routing.py
|           +-- settings.py
|           +-- urls.py
|           \-- wsgi.py
+-- convention.md
+-- exec
|   +-- 1.PORTING_MANUAL.md
|   +-- 3.sarvis_dump_latest.sql
|   \-- 4.presentation_storyboard.md
+-- Jetson
|   +-- .gitignore
|   +-- constraints.txt
|   +-- requirements.txt
|   +-- scripts
|   |   \-- install_jetson_env.sh
|   +-- vision_test
|   |   +-- .gitignore
|   |   +-- api_client.py
|   |   +-- app_image_embedding.py
|   |   +-- app_image_embedding_ko.py
|   |   +-- connect_to_pi_v1.py
|   |   +-- create_ap
|   |   +-- directconnecttest.py
|   |   +-- faceTracker.py
|   |   +-- main.py
|   |   +-- rpi_connect.py
|   |   +-- rpi_connect_any.py
|   |   +-- rpi_connect_nf.py
|   |   +-- rpi_connect2.py
|   |   +-- services.py
|   |   +-- test
|   |   |   +-- app_connect_test.py
|   |   |   +-- direction_test.py
|   |   |   +-- embedding_compare.py
|   |   |   +-- embedding_test.py
|   |   |   +-- onnxruntime_gpu.py
|   |   |   +-- onnxruntime_gpu-1.17.0-cp310-cp310-linux_aarch64.whl
|   |   |   +-- recognition.py
|   |   |   +-- register_face.py
|   |   |   +-- take_photo_webcam.py
|   |   |   +-- test.py
|   |   |   \-- test_insightface.py
|   |   +-- track_login.py
|   |   +-- vision.py
|   |   \-- zev.py
|   \-- voice_test
|       +-- .gitignore
|       +-- apps
|       |   \-- vad_record_threaded.py
|       +-- config.py
|       +-- config_tuned.py
|       +-- enroll
|       |   \-- enroll_to_server_test.py
|       +-- kws
|       |   +-- __init__.py
|       |   +-- log_mel.py
|       |   \-- train_dscnn.py
|       +-- pipeline
|       |   +-- __init__.py
|       |   +-- command_classifier.py
|       |   +-- kws_wake.py
|       |   +-- router.py
|       |   +-- speaker_verify.py
|       |   +-- state_machine.py
|       |   \-- stt_llm.py
|       +-- README.md
|       +-- stt_out.json
|       +-- sv_report.json
|       +-- test
|       |   \-- rms_meter.py
|       +-- tools
|       |   +-- compare_models.py
|       |   +-- complete_pipeline.sh
|       |   +-- convert_wespeaker_to_onnx.py
|       |   +-- debug_voice_pipeline.py
|       |   +-- make_val_from_train.py
|       |   +-- record_long.py
|       |   +-- safe_data_pipeline.py
|       |   +-- silence_split.py
|       |   +-- split_unknown_silence.py
|       |   +-- train_kws_improved.py
|       |   +-- Training_Guide.md
|       |   +-- vad_crop_to_train.py
|       |   \-- validate_wake_word.py
|       +-- voice_api_server.py
|       \-- voice_enroll_server.py
+-- JINWOO
|   +-- arm
|   |   +-- maxrec.py
|   |   +-- mk4.py
|   |   +-- mk5.py
|   |   +-- prototype.py
|   |   +-- rectangle_ver1.py
|   |   +-- sample.y
|   |   +-- samplecode.py
|   |   +-- sixmotor.py
|   |   +-- testarm.py
|   |   +-- testrec.py
|   |   +-- v2proto.py
|   |   \-- yzrectangle.py
|   +-- moniterdev
|   |   +-- phone.py
|   |   \-- READNE0121.md
|   +-- OMX-AI(Follower).stp
|   +-- README26.01.12.md
|   +-- README26.01.13 .md
|   +-- README26.01.14
|   \-- README26.01.15.md
+-- presentation_ppt.pdf
+-- README.md
+-- SARVIS_app
|   +-- FOREGROUND_SERVICE_GUIDE.md
|   +-- sarvis
|   |   +-- .easignore
|   |   +-- .gitignore
|   |   +-- .vscode
|   |   |   +-- extensions.json
|   |   |   \-- settings.json
|   |   +-- api
|   |   |   +-- auth.ts
|   |   |   +-- biometric.ts
|   |   |   +-- client.ts
|   |   |   +-- control.ts
|   |   |   +-- preset.ts
|   |   |   +-- robot.ts
|   |   |   +-- session.ts
|   |   |   +-- types.ts
|   |   |   \-- websocket.ts
|   |   +-- app
|   |   |   +-- (auth)
|   |   |   |   +-- _layout.tsx
|   |   |   |   +-- face-capture.tsx
|   |   |   |   +-- face-reregister.tsx
|   |   |   |   +-- find-id.tsx
|   |   |   |   +-- find-password.tsx
|   |   |   |   +-- login.tsx
|   |   |   |   +-- login-face.tsx
|   |   |   |   +-- login-id.tsx
|   |   |   |   +-- preset-selection.tsx
|   |   |   |   +-- signup.tsx
|   |   |   |   +-- signup-info.tsx
|   |   |   |   +-- voice-register.tsx
|   |   |   |   \-- voice-reregister.tsx
|   |   |   +-- (tabs)
|   |   |   |   +-- _layout.tsx
|   |   |   |   +-- explore.tsx
|   |   |   |   +-- index.tsx
|   |   |   |   +-- preset-manage.tsx
|   |   |   |   +-- preset-select.tsx
|   |   |   |   +-- profile.tsx
|   |   |   |   \-- settings.tsx
|   |   |   +-- _layout.tsx
|   |   |   +-- device-info.tsx
|   |   |   +-- index.tsx
|   |   |   +-- privacy.tsx
|   |   |   \-- terms.tsx
|   |   +-- app.json
|   |   +-- app.zip
|   |   +-- assets
|   |   |   +-- images
|   |   |   |   +-- android-icon-background.png
|   |   |   |   +-- android-icon-foreground.png
|   |   |   |   +-- android-icon-monochrome.png
|   |   |   |   +-- favicon.png
|   |   |   |   +-- icon.png
|   |   |   |   +-- partial-react-logo.png
|   |   |   |   +-- react-logo.png
|   |   |   |   +-- react-logo@2x.png
|   |   |   |   +-- react-logo@3x.png
|   |   |   |   \-- splash-icon.png
|   |   |   \-- sounds
|   |   |       \-- dding.mp3
|   |   +-- clear-auth.js
|   |   +-- com.facebook.react.devsupport.BundleDownloader
|   |   +-- com.facebook.react.devsupport.BundleDownloader$processMultipartResponse$completed$1
|   |   +-- components
|   |   |   +-- biometric
|   |   |   |   \-- FaceCapture.tsx
|   |   |   +-- sarvis
|   |   |   |   +-- connectivity-overlay.tsx
|   |   |   |   +-- sarvis-app-header.tsx
|   |   |   |   +-- sarvis-button.tsx
|   |   |   |   +-- sarvis-footer.tsx
|   |   |   |   +-- sarvis-logo.tsx
|   |   |   |   +-- sarvis-menu-modal.tsx
|   |   |   |   +-- sarvis-screen.tsx
|   |   |   |   +-- sarvis-slider.tsx
|   |   |   |   \-- voice-command-overlay.tsx
|   |   |   \-- youtube
|   |   |       \-- youtube-controller.tsx
|   |   +-- constants
|   |   |   +-- config.ts
|   |   |   \-- sarvis-theme.ts
|   |   +-- eas.json
|   |   +-- eslint.config.js
|   |   +-- force_update.tmp
|   |   +-- modules
|   |   |   +-- YouTubeControlModule.js
|   |   |   \-- YouTubeHandsfreeControl.js
|   |   +-- package.json
|   |   +-- package-lock.json
|   |   +-- providers
|   |   |   +-- auth-provider.tsx
|   |   |   \-- connectivity-provider.tsx
|   |   +-- services
|   |   |   \-- ForegroundService.ts
|   |   +-- test-preset-storage.js
|   |   +-- tsconfig.json
|   |   \-- utils
|   |       +-- Permissions.ts
|   |       +-- presetStorage.ts
|   |       +-- userStorage.ts
|   |       \-- voiceCommandHandler.ts
|   +-- sarvis_mock.css
|   +-- sarvis_mock.html
|   +-- sarvis_mock.js
|   +-- websocket_guide.md
|   \-- websocket_integration_guide.md
+-- SARVIS_app.zip
+-- 김대연
|   +-- readme_0112.md
|   +-- readme_0113.md
|   +-- readme_0114.md
|   +-- readme_0115.md
|   +-- readme_0116.md
|   \-- work
|       +-- .gitignore
|       +-- api명세서.md
|       +-- BACKEND
|       |   +-- djangopjt
|       |   |   +-- .gitignore
|       |   |   +-- accounts
|       |   |   |   +-- __init__.py
|       |   |   |   +-- admin.py
|       |   |   |   +-- apps.py
|       |   |   |   +-- auth_utils.py
|       |   |   |   +-- decorators.py
|       |   |   |   +-- migrations
|       |   |   |   |   +-- __init__.py
|       |   |   |   |   \-- 0001_initial.py
|       |   |   |   +-- models.py
|       |   |   |   +-- serializers.py
|       |   |   |   +-- tests.py
|       |   |   |   +-- urls.py
|       |   |   |   \-- views.py
|       |   |   +-- manage.py
|       |   |   +-- requirements.txt
|       |   |   \-- server
|       |   |       +-- __init__.py
|       |   |       +-- asgi.py
|       |   |       +-- settings.py
|       |   |       +-- urls.py
|       |   |       \-- wsgi.py
|       |   +-- jetson_requirements.txt
|       |   +-- jetson_test_server.py
|       |   \-- package-lock.json
|       +-- FACE_UPLOAD_TEST_GUIDE.md
|       +-- FRONTEND
|       |   +-- sarvis
|       |   |   +-- .gitignore
|       |   |   +-- .vscode
|       |   |   |   +-- extensions.json
|       |   |   |   \-- settings.json
|       |   |   +-- app
|       |   |   |   +-- (auth)
|       |   |   |   |   +-- _layout.tsx
|       |   |   |   |   +-- login.tsx
|       |   |   |   |   +-- login-face.tsx
|       |   |   |   |   +-- login-id.tsx
|       |   |   |   |   +-- signup.tsx
|       |   |   |   |   +-- signup-device.tsx
|       |   |   |   |   +-- signup-face.tsx
|       |   |   |   |   +-- signup-info.tsx
|       |   |   |   |   \-- signup-voice.tsx
|       |   |   |   +-- (tabs)
|       |   |   |   |   +-- _layout.tsx
|       |   |   |   |   +-- explore.tsx
|       |   |   |   |   +-- index.tsx
|       |   |   |   |   \-- softap-test.tsx
|       |   |   |   +-- _layout.tsx
|       |   |   |   +-- device-info.tsx
|       |   |   |   +-- index.tsx
|       |   |   |   \-- modal.tsx
|       |   |   +-- app.json
|       |   |   +-- assets
|       |   |   |   \-- images
|       |   |   |       +-- android-icon-background.png
|       |   |   |       +-- android-icon-foreground.png
|       |   |   |       +-- android-icon-monochrome.png
|       |   |   |       +-- favicon.png
|       |   |   |       +-- icon.png
|       |   |   |       +-- partial-react-logo.png
|       |   |   |       +-- react-logo.png
|       |   |   |       +-- react-logo@2x.png
|       |   |   |       +-- react-logo@3x.png
|       |   |   |       \-- splash-icon.png
|       |   |   +-- components
|       |   |   |   \-- sarvis
|       |   |   |       +-- sarvis-app-header.tsx
|       |   |   |       +-- sarvis-button.tsx
|       |   |   |       +-- sarvis-footer.tsx
|       |   |   |       +-- sarvis-logo.tsx
|       |   |   |       +-- sarvis-screen.tsx
|       |   |   |       \-- sarvis-slider.tsx
|       |   |   +-- constants
|       |   |   |   \-- sarvis-theme.ts
|       |   |   +-- eslint.config.js
|       |   |   +-- package.json
|       |   |   +-- package-lock.json
|       |   |   +-- providers
|       |   |   |   \-- auth-provider.tsx
|       |   |   +-- README.md
|       |   |   +-- tsconfig.json
|       |   |   \-- utils
|       |   |       +-- api.ts
|       |   |       \-- softap-communication.ts
|       |   +-- sarvis_mock.css
|       |   +-- sarvis_mock.html
|       |   \-- sarvis_mock.js
|       +-- JETSON_SOFTAP_SETUP.md
|       +-- LOGIN_FACE_TEST_GUIDE_KR.md
|       +-- NETWORK_TROUBLESHOOTING.md
|       +-- requirements.txt
|       +-- server_test.py
|       +-- SIGNUP_GUIDE.md
|       +-- SOFTAP_TEST_GUIDE.md
|       +-- SOFTAP_TEST_GUIDE_KR.md
|       +-- test_face_upload.js
|       +-- Use_case_revised.md
|       +-- wireframe_architecture.md
|       \-- 기능별_상세_명세.md
+-- 이주선
|   +-- 20260112.md
|   +-- 20260113.md
|   +-- 20260114.md
|   +-- 20260115.md
|   +-- 20260116.md
|   +-- 20260127.md
|   +-- 20260128.md
|   +-- 20260129.md
|   +-- image.png
|   +-- UIUX초안
|   |   +-- sarvis.html
|   |   +-- SARVIS_JOOSUN(3).html
|   |   \-- sarvis_mock.html
|   \-- 아래판.png
+-- 정다진
|   +-- images
|   |   +-- erd.png
|   |   +-- new system architecture.png
|   |   \-- system architecture.png
|   +-- README_260112.md
|   +-- README_260113.md
|   +-- README_260114.md
|   +-- README_260115.md
|   \-- README_260116.md
+-- 정서영
|   +-- image
|   |   \-- erd.png
|   +-- README0112.md
|   +-- README0113.md
|   +-- README0114.md
|   +-- README0115.md
|   \-- README0116.md
\-- 제영호
    +-- README.md
    \-- 일지
        +-- 260112.md
        +-- 260113.md
        +-- 260114.md
        +-- 260115.md
        \-- images
            +-- diagram.jpg
            \-- 시스템아키텍처.png
```
