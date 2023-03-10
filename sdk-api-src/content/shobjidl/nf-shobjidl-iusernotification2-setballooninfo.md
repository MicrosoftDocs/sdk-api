---
UID: NF:shobjidl.IUserNotification2.SetBalloonInfo
title: IUserNotification2::SetBalloonInfo (shobjidl.h)
description: Sets the information to be displayed in a balloon notification. (IUserNotification2.SetBalloonInfo)
helpviewer_keywords: ["IUserNotification2 interface [Windows Shell]","SetBalloonInfo method","IUserNotification2.SetBalloonInfo","IUserNotification2::SetBalloonInfo","NIIF_ERROR","NIIF_ICON_MASK","NIIF_INFO","NIIF_LARGE_ICON","NIIF_NONE","NIIF_NOSOUND","NIIF_RESPECT_QUIET_TIME","NIIF_USER","NIIF_WARNING","SetBalloonInfo","SetBalloonInfo method [Windows Shell]","SetBalloonInfo method [Windows Shell]","IUserNotification2 interface","_shell_IUserNotification2_SetBalloonInfo","shell.IUserNotification2_SetBalloonInfo","shobjidl/IUserNotification2::SetBalloonInfo"]
old-location: shell\IUserNotification2_SetBalloonInfo.htm
tech.root: shell
ms.assetid: 3615F243-1F1B-4b9f-9083-B1EF3B5048DD
ms.date: 12/05/2018
ms.keywords: IUserNotification2 interface [Windows Shell],SetBalloonInfo method, IUserNotification2.SetBalloonInfo, IUserNotification2::SetBalloonInfo, NIIF_ERROR, NIIF_ICON_MASK, NIIF_INFO, NIIF_LARGE_ICON, NIIF_NONE, NIIF_NOSOUND, NIIF_RESPECT_QUIET_TIME, NIIF_USER, NIIF_WARNING, SetBalloonInfo, SetBalloonInfo method [Windows Shell], SetBalloonInfo method [Windows Shell],IUserNotification2 interface, _shell_IUserNotification2_SetBalloonInfo, shell.IUserNotification2_SetBalloonInfo, shobjidl/IUserNotification2::SetBalloonInfo
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUserNotification2::SetBalloonInfo
 - shobjidl/IUserNotification2::SetBalloonInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IUserNotification2.SetBalloonInfo
---

# IUserNotification2::SetBalloonInfo


## -description

Sets the information to be displayed in a balloon notification.

## -parameters

### -param pszTitle [in]

Type: <b>LPCWSTR</b>

A pointer to a Unicode string that specifies the title of the notification.

### -param pszText [in]

Type: <b>LPCWSTR</b>

A pointer to a Unicode string that specifies the text to be displayed in the body of the balloon.

### -param dwInfoFlags [in]

Type: <b>DWORD</b>

One or more of the following values that indicate an icon to display in the notification balloon.



#### NIIF_NONE (0x00000000)

0x00000000. Do not display an icon.



#### NIIF_INFO (0x00000001)

0x00000001. Display an information icon.



#### NIIF_WARNING (0x00000002)

0x00000002. Display a warning icon.



#### NIIF_ERROR (0x00000003)

0x00000003. Display an error icon.



#### NIIF_USER (0x00000004)

0x00000004. <b>Windows XP SP2 and later</b>. Use the icon identified in <b>hIcon</b> in the notification balloon.



#### NIIF_NOSOUND (0x00000010)

0x00000010. <b>Windows XP and later</b>. Do not play the associated sound. This value applies only to balloon notifications and not to standard user notifications.



#### NIIF_LARGE_ICON (0x00000010)

0x00000010. <b>Windows Vista and later</b>. The large version of the icon should be used as the icon in the notification balloon. This corresponds to the icon with dimensions SM_CXICON x SM_CYICON. If this flag is not set, the icon with dimensions XM_CXSMICON x SM_CYSMICON is used. 

                        

<ul>
<li>This flag can be used with all <a href="/windows/desktop/api/shellapi/ne-shellapi-shstockiconid">stock icons</a>.</li>
<li>Applications that use older customized icons (NIIF_USER with <b>hIcon</b>) must provide a new SM_CXICON x SM_CYICON version in the tray icon specified in the <b>hIcon</b> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa">NOTIFYICONDATA</a> structure. These icons are scaled down when they are displayed in the notification area.</li>
<li>New customized icons (NIIF_USER with <b>hBalloonIcon</b>) must supply an SM_CXICON x SM_CYICON version in the supplied icon (<b>hBalloonIcon</b>).</li>
</ul>


#### NIIF_RESPECT_QUIET_TIME (0x00000080)

0x00000080. <b>Windows 7 and later</b>. Do not display the notification balloon if the current user is in "quiet time", which is the first hour after a new user logs into his or her account for the first time. During this time, most notifications should not be sent or shown. This lets a user become accustomed to a new computer system without those distractions. Quiet time also occurs for each user after an operating system upgrade or clean installation. A notification sent with this flag during quiet time is not queued; it is simply dismissed unshown. The application can resend the notification later if it is still valid at that time.

Because an application cannot predict when it might encounter quiet time, we recommended that this flag always be set on all appropriate notifications by any application that means to honor quiet time.

If the current user is not in quiet time, this flag has no effect.



#### NIIF_ICON_MASK (0x0000000F)

0x0000000F. <b>Windows XP</b> (<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Shell32.dll version 6.0</a><b>) and later</b>. Reserved.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusernotification2">IUserNotification2</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-setballooninfo">SetBalloonInfo</a>
