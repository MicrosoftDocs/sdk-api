---
UID: NS:msctf.TF_SELECTION
title: TF_SELECTION
author: windows-driver-content
description: The TF_SELECTION structure contains text selection data.
old-location: tsf\tf_selection.htm
old-project: TSF
ms.assetid: c844a6d1-b3b9-49cf-83a6-1ee8b3bd2d54
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: TF_SELECTION, TF_SELECTION structure [Text Services Framework], _tsf_tf_selection_ref, msctf/TF_SELECTION, tsf.tf_selection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_SELECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Msctf.h
api_name:
-	TF_SELECTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# TF_SELECTION structure


## -description



The <b>TF_SELECTION</b> structure contains text selection data.




## -struct-fields




### -field range

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that specifies the selected text.


### -field style

A <a href="https://msdn.microsoft.com/3a38172b-611b-445f-be24-ea2a19178255">TF_SELECTIONSTYLE</a> structure that contains selection data.


## -see-also




<a href="https://msdn.microsoft.com/08b67fd5-aebe-49f7-af78-6f49c8f47f64">ITfContext::GetSelection
      </a>



<a href="https://msdn.microsoft.com/1cf50b5e-6ec2-4649-9acc-743a2e3d8096">
        ITfContext::SetSelection
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">
        ITfRange
      </a>



<a href="https://msdn.microsoft.com/3a38172b-611b-445f-be24-ea2a19178255">
        TF_SELECTIONSTYLE
      </a>
 

 

