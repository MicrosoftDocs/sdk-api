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

# IExpDispSupport::OnTranslateAccelerator


## -description


Deprecated. Instructs the control site to process the keystroke described in <i>pMsg</i> and modified by the flags in <i>grfModifiers</i>.


## -parameters




### -param pMsg

Type: <b><a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a> structure that describes the keystroke to be processed.


### -param grfModifiers

Type: <b>DWORD</b>

Flags describing the state of the CTRL, ALT, and SHIFT keys. The value of the flags can be any valid <a href="https://msdn.microsoft.com/5a85158d-33a7-4c99-a636-42f7c68dc3ce">KEYMODIFIERS</a> enumeration value or values.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the container processed the message, <b>S_FALSE</b> if the container did not process the message, or <b>E_NOTIMPL</b> if the container does not implement accelerator support.



