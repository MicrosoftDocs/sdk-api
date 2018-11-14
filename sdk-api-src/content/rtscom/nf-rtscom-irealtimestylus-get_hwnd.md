---
UID: NF:rtscom.IRealTimeStylus.get_HWND
title: IRealTimeStylus::get_HWND
author: windows-sdk-content
description: Gets or sets the handle value associated with the window the RealTimeStylus object uses.
old-location: tablet\irealtimestylus_hwnd.htm
tech.root: tablet
ms.assetid: b6bc8053-80fa-45f3-8096-272b471a5f6d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: HWND property [Tablet PC], HWND property [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],HWND property, IRealTimeStylus.HWND, IRealTimeStylus.get_HWND, IRealTimeStylus.put_HWND, IRealTimeStylus::HWND, IRealTimeStylus::get_HWND, IRealTimeStylus::put_HWND, b6bc8053-80fa-45f3-8096-272b471a5f6d, get_HWND, rtscom/IRealTimeStylus::HWND, rtscom/IRealTimeStylus::get_HWND, rtscom/IRealTimeStylus::put_HWND, tablet.irealtimestylus_hwnd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: RTSCom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylus.HWND
 - IRealTimeStylus.get_HWND
 - IRealTimeStylus.put_HWND
 - IRealTimeStylus.get_HWND
 - IRealTimeStylus.put_HWND
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- rtscom.h
: 
- IRealTimeStylus.get_HWND
: 
---

# IRealTimeStylus::get_HWND


## -description



Gets or sets the handle value associated with the window the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object uses.



This property is read/write.


## -parameters


## -remarks



If two or more windows exist, this property allows you to specify which window collects ink.

The HRESULT E_INVALIDOPERATION is returned when you attempt set this property on a child <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object.




## -see-also




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/e96e27d7-b453-49a7-b684-b3dd5f94c378">IRealTimeStylus::Enabled Property</a>



<b>RealTimeStylus Class</b>



<a href="https://msdn.microsoft.com/a239b53c-7fc9-4211-962a-6cfbe0be4e4c">RealTimeStylus Reference</a>
 

 

