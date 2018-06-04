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

# DSEditSecurity function


## -description


The <b>DSEditSecurity</b> function displays a modal dialog box for editing security on a Directory Services (DS) object.


## -parameters




### -param hwndOwner [in]

The dialog box owner window.


### -param pwszObjectPath [in]

The full Active Directory Services (ADS) path of the DS object.


### -param pwszObjectClass [in, optional]

The class of the object.


### -param dwFlags [in]

The combination of DSSI_* flags.


### -param pwszCaption [in, optional]

The dialog box caption.


### -param pfnReadSD [in, optional]

The function for reading the object.


### -param pfnWriteSD [in, optional]

The function for writing the object.


### -param lpContext [in]

The context passed into the read or write functions in the <i>pfnReadSD</i> and <i>pfnWriteSD</i> parameters.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



