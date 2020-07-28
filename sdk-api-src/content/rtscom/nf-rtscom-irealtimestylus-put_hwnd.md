---
UID: NF:rtscom.IRealTimeStylus.put_HWND
title: IRealTimeStylus::put_HWND (rtscom.h)
description: Gets or sets the handle value associated with the window the RealTimeStylus object uses.
helpviewer_keywords: ["HWND property [Tablet PC]","HWND property [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","HWND property","IRealTimeStylus.HWND","IRealTimeStylus.get_HWND","IRealTimeStylus.put_HWND","IRealTimeStylus::HWND","IRealTimeStylus::get_HWND","IRealTimeStylus::put_HWND","b6bc8053-80fa-45f3-8096-272b471a5f6d","put_HWND","rtscom/IRealTimeStylus::HWND","rtscom/IRealTimeStylus::get_HWND","rtscom/IRealTimeStylus::put_HWND","tablet.irealtimestylus_hwnd"]
old-location: tablet\irealtimestylus_hwnd.htm
tech.root: tablet
ms.assetid: b6bc8053-80fa-45f3-8096-272b471a5f6d
ms.date: 12/05/2018
ms.keywords: HWND property [Tablet PC], HWND property [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],HWND property, IRealTimeStylus.HWND, IRealTimeStylus.get_HWND, IRealTimeStylus.put_HWND, IRealTimeStylus::HWND, IRealTimeStylus::get_HWND, IRealTimeStylus::put_HWND, b6bc8053-80fa-45f3-8096-272b471a5f6d, put_HWND, rtscom/IRealTimeStylus::HWND, rtscom/IRealTimeStylus::get_HWND, rtscom/IRealTimeStylus::put_HWND, tablet.irealtimestylus_hwnd
f1_keywords:
- rtscom/IRealTimeStylus.HWND
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRealTimeStylus::put_HWND


## -description



Gets or sets the handle value associated with the window the <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object uses.



This property is read/write.


## -parameters


## -remarks



If two or more windows exist, this property allows you to specify which window collects ink.

The HRESULT E_INVALIDOPERATION is returned when you attempt set this property on a child <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-get_enabled">IRealTimeStylus::Enabled Property</a>



<b>RealTimeStylus Class</b>



<a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-reference">RealTimeStylus Reference</a>
 

 

