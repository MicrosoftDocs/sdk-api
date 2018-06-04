---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUserNotification::SetBalloonInfo


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
<li>This flag can be used with all <a href="https://msdn.microsoft.com/37da5555-3626-465e-b834-3a28b75495c4">stock icons</a>.</li>
<li>Applications that use older customized icons (NIIF_USER with <b>hIcon</b>) must provide a new SM_CXICON x SM_CYICON version in the tray icon specified in the <b>hIcon</b> member of the <a href="https://msdn.microsoft.com/fdcc42c1-b3e5-4b04-8d79-7b6c29699d53">NOTIFYICONDATA</a> structure. These icons are scaled down when they are displayed in the notification area.</li>
<li>New customized icons (NIIF_USER with <b>hBalloonIcon</b>) must supply an SM_CXICON x SM_CYICON version in the supplied icon (<b>hBalloonIcon</b>).</li>
</ul>


#### NIIF_RESPECT_QUIET_TIME (0x00000080)

0x00000080. <b>Windows 7 and later</b>. Do not display the notification balloon if the current user is in "quiet time", which is the first hour after a new user logs into his or her account for the first time. During this time, most notifications should not be sent or shown. This lets a user become accustomed to a new computer system without those distractions. Quiet time also occurs for each user after an operating system upgrade or clean installation. A notification sent with this flag during quiet time is not queued; it is simply dismissed unshown. The application can resend the notification later if it is still valid at that time.

Because an application cannot predict when it might encounter quiet time, we recommended that this flag always be set on all appropriate notifications by any application that means to honor quiet time.

If the current user is not in quiet time, this flag has no effect.



#### NIIF_ICON_MASK (0x0000000F)

0x0000000F. <b>Windows XP</b> (<a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Shell32.dll version 6.0</a><b>) and later</b>. Reserved.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



