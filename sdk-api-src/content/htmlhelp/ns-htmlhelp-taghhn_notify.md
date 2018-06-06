---
UID: NS:htmlhelp.tagHHN_NOTIFY
title: tagHHN_NOTIFY
author: windows-sdk-content
description: Use this structure to return the file name of the topic that has been navigated to, or to return the window type name of the help window that has been created.
old-location: htmlhelp\hhn_notify_structure.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\vsconstrhhnnotify.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: HHN_NOTIFY, HHN_NOTIFY structure [HTML Help Workshop], htmlhelp.hhn_notify_structure, htmlhelp/HHN_NOTIFY, tagHHN_NOTIFY, vsconStrhhnnotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: HHN_NOTIFY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - HtmlHelp.h
api_name:
 - HHN_NOTIFY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagHHN_NOTIFY structure


## -description


Use this structure to return the file name of the topic that has been navigated to, or to return the window type name of the help window that has been created.


## -struct-fields




### -field hdr

Standard <b>WM_NOTIFY</b> header. 


### -field pszUrl

A multi-byte, zero-terminated string that specifies the topic navigated to, or the name of the help window being created. 


## -see-also




<a href="https://msdn.microsoft.com/E75CA82E-9759-47d8-AF84-5842EDAB019D">About Structures</a>
 

 

