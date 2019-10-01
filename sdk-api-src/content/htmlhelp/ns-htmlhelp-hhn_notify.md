---
UID: NS:htmlhelp.tagHHN_NOTIFY
title: HHN_NOTIFY (htmlhelp.h)
author: windows-sdk-content
description: Use this structure to return the file name of the topic that has been navigated to, or to return the window type name of the help window that has been created.
old-location: htmlhelp\hhn_notify_structure.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\vsconstrhhnnotify.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HHN_NOTIFY, HHN_NOTIFY structure [HTML Help Workshop], htmlhelp.hhn_notify_structure, htmlhelp/HHN_NOTIFY, vsconStrhhnnotify
ms.topic: struct
f1_keywords: 
 - "htmlhelp/HHN_NOTIFY"
req.header: htmlhelp.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - HtmlHelp.h
api_name:
 - HHN_NOTIFY
targetos: Windows
req.typenames: HHN_NOTIFY
req.redist: 
ms.custom: 19H1
---

# HHN_NOTIFY structure


## -description


Use this structure to return the file name of the topic that has been navigated to, or to return the window type name of the help window that has been created.


## -struct-fields




### -field hdr

Standard <b>WM_NOTIFY</b> header. 


### -field pszUrl

A multi-byte, zero-terminated string that specifies the topic navigated to, or the name of the help window being created. 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/htmlhelp/about-structures">About Structures</a>
 

 

