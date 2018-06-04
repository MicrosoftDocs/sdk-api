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

# _MI_UtilitiesFT structure


## -description


A support structure used in the 
   <a href="https://msdn.microsoft.com/9c8c812d-d91d-4754-9be5-c05360364b1b">MI_ClientFT_V1</a> structure. Use the functions with the 
   name prefix "MI_Utilities_" to manipulate these structures.


## -struct-fields






#### - CimErrorFromErrorCode

Maps an operating-system specific error code to a CIM error instance. See 
   <a href="https://msdn.microsoft.com/dab6226b-5769-4e2f-abd2-b89cc2d9911e">MI_Utilities_CimErrorFromErrorCode</a>.


#### - MapErrorToExtendedError

This function has been deprecated. See 
   <a href="https://msdn.microsoft.com/cbd5bd18-897d-49ce-82b7-98f97c3c02d7">MI_Utilities_MapErrorToExtendedError</a>.


#### - MapErrorToMiErrorCategory

This function has been deprecated. See 
   <a href="https://msdn.microsoft.com/58ac8e3e-ae87-40b1-bf27-1b32168a033e">MI_Utilities_MapErrorToMiErrorCategory</a>.

