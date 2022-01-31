---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0000_0007
title: RDPSRAPI_WND_FLAGS (rdpencomapi.h)
description: Defines values for the type of window.
helpviewer_keywords: ["RDPSRAPI_WND_FLAGS","RDPSRAPI_WND_FLAGS enumeration [RDP]","WND_FLAG_PRIVILEGED","rdp.rdpsrapi_wnd_flags","rdpencomapi/RDPSRAPI_WND_FLAGS","rdpencomapi/WND_FLAG_PRIVILEGED"]
old-location: rdp\rdpsrapi_wnd_flags.htm
tech.root: rdp
ms.assetid: 0ba626e0-b6dc-4331-9541-0c27c73b3de4
ms.date: 12/05/2018
ms.keywords: RDPSRAPI_WND_FLAGS, RDPSRAPI_WND_FLAGS enumeration [RDP], WND_FLAG_PRIVILEGED, rdp.rdpsrapi_wnd_flags, rdpencomapi/RDPSRAPI_WND_FLAGS, rdpencomapi/WND_FLAG_PRIVILEGED
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
targetos: Windows
req.typenames: RDPSRAPI_WND_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_rdpencomapi_0000_0000_0007
 - rdpencomapi/__MIDL___MIDL_itf_rdpencomapi_0000_0000_0007
 - RDPSRAPI_WND_FLAGS
 - rdpencomapi/RDPSRAPI_WND_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rdpencomapi.h
api_name:
 - RDPSRAPI_WND_FLAGS
---

# RDPSRAPI_WND_FLAGS enumeration


## -description

Defines values for the type of window. These flags can be retrieved from the <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiwindow">IRDPSRAPIWindow</a> interface that represents each Win32 window.

The list of windows on the sharing user session can be retrieved on both the sharer and the viewer through the <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiapplicationfilter">IRDPSRAPIApplicationFilter</a> interface by calling the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiapplicationfilter-get_windows">get_Windows</a> method.

## -enum-fields

### -field WND_FLAG_PRIVILEGED:1

The window is part of an application that runs at a higher level than the current process. This flag indicates that the window cannot be shared. Applications can use this flag to prevent the user from sharing it either by disabling the entry for the window in the user interface or by not showing the entry.

## -see-also

<a href="/previous-versions/windows/desktop/rdp/windows-desktop-sharing-enumerations">Windows Desktop Sharing Enumerations</a>
