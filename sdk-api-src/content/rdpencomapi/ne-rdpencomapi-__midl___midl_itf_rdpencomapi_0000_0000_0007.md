---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0000_0007
title: "__MIDL___MIDL_itf_rdpencomapi_0000_0000_0007"
author: windows-sdk-content
description: Defines values for the type of window.
old-location: rdp\rdpsrapi_wnd_flags.htm
tech.root: Rdp
ms.assetid: 0ba626e0-b6dc-4331-9541-0c27c73b3de4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RDPSRAPI_WND_FLAGS, RDPSRAPI_WND_FLAGS enumeration [RDP], WND_FLAG_PRIVILEGED, __MIDL___MIDL_itf_rdpencomapi_0000_0000_0007, rdp.rdpsrapi_wnd_flags, rdpencomapi/RDPSRAPI_WND_FLAGS, rdpencomapi/WND_FLAG_PRIVILEGED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rdpencomapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rdpencomapi.h
api_name:
 - RDPSRAPI_WND_FLAGS
product: Windows
targetos: Windows
req.typenames: RDPSRAPI_WND_FLAGS
req.redist: 
---

# __MIDL___MIDL_itf_rdpencomapi_0000_0000_0007 enumeration


## -description


Defines values for the type of window. These flags can be retrieved from the <a href="https://msdn.microsoft.com/85c8263b-e796-4748-b8e5-6315e5937861">IRDPSRAPIWindow</a> interface that represents each Win32 window.

The list of windows on the sharing user session can be retrieved on both the sharer and the viewer through the <a href="https://msdn.microsoft.com/6a08c948-1b25-4a36-93c8-23e7e3f4fb08">IRDPSRAPIApplicationFilter</a> interface by calling the <a href="https://msdn.microsoft.com/cc964964-0f3a-410c-b1f4-426abd9c1a22">get_Windows</a> method.


## -enum-fields




### -field WND_FLAG_PRIVILEGED

The window is part of an application that runs at a higher level than the current process. This flag indicates that the window cannot be shared. Applications can use this flag to prevent the user from sharing it either by disabling the entry for the window in the user interface or by not showing the entry.


## -see-also




<a href="https://msdn.microsoft.com/ceda755a-dd9a-4d89-96b2-39e2dca46801">Windows Desktop Sharing Enumerations</a>
 

 

