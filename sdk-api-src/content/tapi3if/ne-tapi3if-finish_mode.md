---
UID: NE:tapi3if.FINISH_MODE
title: FINISH_MODE
author: windows-sdk-content
description: The FINISH_MODE enum is used by applications to indicate the type of call finish required. Operations that the TAPI DLL performs vary depending on whether a call transfer is being completed or a call is being added to a conference.
old-location: tapi3\finish_mode.htm
tech.root: tapi
ms.assetid: f0bf1d93-b6c3-473a-b7ee-2ebb984f42c5
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: FINISH_MODE, FINISH_MODE enumeration [TAPI 2.2], FM_ASCONFERENCE, FM_ASTRANSFER, _tapi3_finish_mode, tapi3.finish_mode, tapi3if/FINISH_MODE, tapi3if/FM_ASCONFERENCE, tapi3if/FM_ASTRANSFER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tapi3if.h
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
 - Tapi3if.h
api_name:
 - FINISH_MODE
product: Windows
targetos: Windows
req.typenames: FINISH_MODE
req.redist: 
---

# FINISH_MODE enumeration


## -description


The 
<b>FINISH_MODE</b> enum is used by applications to indicate the type of call finish required. Operations that the TAPI DLL performs vary depending on whether a call transfer is being completed or a call is being added to a conference.


## -enum-fields




### -field FM_ASTRANSFER

A call transfer is being finished.


### -field FM_ASCONFERENCE

A call is being added to a conference call.


## -see-also




<a href="https://msdn.microsoft.com/3b0bd871-b618-4c24-a717-62a248112d97">ITBasicCallControl::Finish</a>
 

 

