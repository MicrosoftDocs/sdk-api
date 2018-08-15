---
UID: NE:shappmgr._tagPublishedAppInfoFlags
title: "_tagPublishedAppInfoFlags"
author: windows-sdk-content
description: Specifies which members in the PUBAPPINFO structure are valid. These flags are bitmasks set in the dwMask member and passed to IPublishedApp::GetPublishedAppInfo.
old-location: shell\PUBAPPINFOFLAGS.htm
old-project: shell
ms.assetid: 9fcb93a5-24b5-4bc3-9f20-0088affb183b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PAI_ASSIGNEDTIME, PAI_EXPIRETIME, PAI_PUBLISHEDTIME, PAI_SCHEDULEDTIME, PAI_SOURCE, PUBAPPINFOFLAGS, PUBAPPINFOFLAGS enumeration [Windows Shell], _tagPublishedAppInfoFlags, inet_PUBAPPINFOFLAGS, shappmgr/PAI_ASSIGNEDTIME, shappmgr/PAI_EXPIRETIME, shappmgr/PAI_PUBLISHEDTIME, shappmgr/PAI_SCHEDULEDTIME, shappmgr/PAI_SOURCE, shappmgr/PUBAPPINFOFLAGS, shell.PUBAPPINFOFLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shappmgr.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PUBAPPINFOFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shappmgr.h
api_name:
 - PUBAPPINFOFLAGS
product: Windows
targetos: Windows
req.lib: Sfc.lib
req.dll: Sfc.dll
req.irql: 
req.product: ADAM
---

# _tagPublishedAppInfoFlags enumeration


## -description


Specifies which members in the <a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">PUBAPPINFO</a> structure are valid. These flags are bitmasks set in the <b>dwMask</b> member and passed to <a href="https://msdn.microsoft.com/4ffcc30a-cf07-45e7-b9a5-342fe2b553c8">IPublishedApp::GetPublishedAppInfo</a>.


## -enum-fields




### -field PAI_SOURCE

The <a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">pszSource</a> string is valid and contains the display name of the publishing source. If multiple sources publish an application of the same name, Add/Remove Programs identifies them by "&lt;application name&gt; : &lt;publishing source&gt;".


### -field PAI_ASSIGNEDTIME

The <a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">stAssigned</a> member is valid and contains the time that the application should be installed as assigned by an application administrator.


### -field PAI_PUBLISHEDTIME

Not used.


### -field PAI_SCHEDULEDTIME

The <a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">stScheduled</a> member is valid and contains the time that the application should be installed as assigned by the user.


### -field PAI_EXPIRETIME

The <a href="https://msdn.microsoft.com/927c58d3-4208-4fd3-a3fa-18ae7d8d3136">stExpired</a> member is valid and contains the time after which Add/Remove Programs should no longer install the program.


## -see-also




<a href="https://msdn.microsoft.com/4ffcc30a-cf07-45e7-b9a5-342fe2b553c8">IPublishedApp::GetPublishedAppInfo</a>
 

 

