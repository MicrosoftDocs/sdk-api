---
UID: NS:mi._MI_FilterFT
title: "_MI_FilterFT"
author: windows-sdk-content
description: A support structure used in the MI_Filter structure. Use the functions with the name prefix &#0034;MI_Filter_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_filterft.htm
old-project: wmi_v2
ms.assetid: f090b05e-e99b-47aa-8458-8e2cf9031ac7
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_FilterFT, MI_FilterFT structure [Windows Management Infrastructure (MI)], _MI_FilterFT, mi/MI_FilterFT, wmi_v2.mi_filterft
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
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
tech.root: 
req.typenames: MI_FilterFT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_FilterFT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_FilterFT structure


## -description


A support structure used in the <a href="https://msdn.microsoft.com/0849cb55-ba2f-4855-ac33-fa96d8ecd94f">MI_Filter</a> 
    structure. Use the functions with the name prefix "MI_Filter_" to manipulate these 
    structures.


## -struct-fields






#### - Evaluate

The provider calls this function to evaluate an instance against a given filter. See 
       <a href="https://msdn.microsoft.com/b826f02d-3764-4f61-996f-42bf01ea44e2">MI_Filter_Evaluate</a>.


#### - GetExpression

Gets the filter language and expression. See 
       <a href="https://msdn.microsoft.com/a1ba9cf2-b613-4621-a4ac-39808b4bfd8e">MI_Filter_GetExpression</a>.

