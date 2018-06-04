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

# IEnumWIA_DEV_CAPS::Next


## -description


The <b>IEnumWIA_DEV_CAPS::Next</b> method fills an array of pointers to <a href="https://msdn.microsoft.com/9bf123c7-234f-45d3-bb45-c0cb135ef970">WIA_DEV_CAP</a> structures.



## -parameters




### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of array elements in the array indicated by the <i>rgelt</i> parameter.


### -param rgelt [out]

Type: <b><a href="https://msdn.microsoft.com/9bf123c7-234f-45d3-bb45-c0cb135ef970">WIA_DEV_CAP</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/9bf123c7-234f-45d3-bb45-c0cb135ef970">WIA_DEV_CAP</a> structures. <b>IEnumWIA_DEV_CAPS::Next</b> fills this array of structures.


### -param pceltFetched [in, out]

Type: <b>ULONG*</b>

On output, this parameter contains the number of structure pointers actually stored in the array indicated by the <i>rgelt</i> parameter.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications use this method to query the capabilities of each available Windows Image Acquisition (WIA) hardware device. To do so, the application passes a pointer to an array of <a href="https://msdn.microsoft.com/9bf123c7-234f-45d3-bb45-c0cb135ef970">WIA_DEV_CAP</a> structures that it allocates. It also passes in the number of array elements in the parameter <i>celt</i>. The <b>IEnumWIA_DEV_CAPS::Next</b> method fills the array with structures. Applications then use the structures to enumerate WIA hardware device capabilities.

WIA device capabilities are defined as events and commands that the device supports. Using the <i>rgelt</i> array, <b>IEnumWIA_DEV_CAPS::Next</b> passes a single structure to the application for each event and command that the device supports.

Note that <b>IEnumWIA_DEV_CAPS::Next</b> dynamically allocates the <a href="https://msdn.microsoft.com/9bf123c7-234f-45d3-bb45-c0cb135ef970">WIA_DEV_CAP</a> structures it provides to applications. Therefore, applications must delete the <b>WIA_DEV_CAP</b> structures they receive through the <i>rgelt</i> parameter. Applications should use <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the <i>bstrName</i>, <i>bstrDescription</i>, and <i>bstrIcon</i> fields of all <b>WIA_DEV_CAP</b> structures.



