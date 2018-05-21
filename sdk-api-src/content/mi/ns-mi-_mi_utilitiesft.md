---
UID: NS:mi._MI_UtilitiesFT
title: "_MI_UtilitiesFT"
author: windows-driver-content
description: A support structure used in the MI_ClientFT_V1 structure. Use the functions with the name prefix &#0034;MI_Utilities_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_utilitiesft.htm
old-project: wmi_v2
ms.assetid: 4f82b7b3-833c-42e8-a80c-2d057fc34fe4
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: MI_UtilitiesFT, MI_UtilitiesFT structure [Windows Management Infrastructure (MI)], _MI_UtilitiesFT, mi/MI_UtilitiesFT, wmi_v2.mi_utilitiesft
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MI_UtilitiesFT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_UtilitiesFT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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

