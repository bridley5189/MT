# 📢 MT - Toast Notification Configuration

[![Repository](https://img.shields.io/badge/Repository-MT-blue?logo=github)](https://github.com/bridley5189/MT)
[![Windows](https://img.shields.io/badge/Platform-Windows-blue.svg?logo=windows)](https://www.microsoft.com/windows)
[![Toast](https://img.shields.io/badge/Type-Toast_Notifications-orange.svg)](https://github.com/bridley5189/MT)

**Windows Toast Notification Templates and Configuration**

---

## 📋 Overview

This repository contains XML configuration files and image assets for creating custom Windows Toast Notifications, specifically designed for iOS update notifications and system alerts.

## 📁 Repository Contents

| File | Type | Description |
|------|------|-------------|
| `config-toast-iosupdate.xml` | Config | Toast notification XML template for iOS updates |
| `ToastHeroImageiOS.png` | Image | Hero image for toast notifications |

## 🎯 Purpose

- **Toast Configuration** - Pre-built XML templates for Windows Toast Notifications
- **Hero Images** - Branded hero images for notification headers
- **iOS Update Alerts** - Specialized templates for iOS device update notifications
- **Reusable Templates** - Easy-to-customize notification configurations

## 🔧 XML Configuration

The toast configuration includes:
- **Hero Image** - Visual header for notifications
- **Title Text** - Notification headline
- **Body Text** - Detailed message content
- **Action Buttons** - User interaction options
- **Attribution** - Source information

## 📱 Use Cases

- **iOS Update Notifications** - Alert users about iOS device updates
- **System Alerts** - Important system notifications
- **User Notifications** - Custom application alerts
- **Endpoint Management** - Intune or SCCM notification templates

## 🛠️ PowerShell Implementation

```powershell
# Load XML configuration
[xml]$toastXml = Get-Content -Path "config-toast-iosupdate.xml"

# Create toast notification
$toast = [Windows.UI.Notifications.ToastNotification]::new($toastXml)

# Display notification
$notifier = [Windows.UI.Notifications.ToastNotificationManager]::CreateToastNotifier()
$notifier.Show($toast)
```

## 📐 XML Structure

```xml
<toast>
    <visual>
        <binding template="ToastGeneric">
            <image placement="hero" src="ToastHeroImageiOS.png"/>
            <text>Update Available</text>
            <text>iOS update notification details</text>
        </binding>
    </visual>
    <actions>
        <!-- Action buttons here -->
    </actions>
</toast>
```

## 🔗 Integration

Can be used with:
- **PowerShell Scripts** - Automated notification systems
- **Intune** - Endpoint management notifications
- **ConfigMgr/SCCM** - Software deployment alerts
- **Custom Applications** - User notification systems

## 📝 Customization

To customize the toast notification:

1. **Update Hero Image** - Replace `ToastHeroImageiOS.png` with your image
2. **Modify XML** - Edit text, buttons, and styling in the XML file
3. **Deploy** - Use in your PowerShell scripts or applications

## 📚 Resources

- [Windows Toast Notification Documentation](https://docs.microsoft.com/en-us/windows/apps/design/shell/tiles-and-notifications/adaptive-interactive-toasts)
- [Toast XML Schema](https://docs.microsoft.com/en-us/windows/apps/design/shell/tiles-and-notifications/toast-xml-schema)

---

<div align="center">

**Part of [bridley5189's GitHub Repositories](https://github.com/bridley5189)**

Compatible with [PowerShell-Applications](https://github.com/bridley5189/Powershell-Applications)

</div>
