---
UID: NS:msctf.TF_PRESERVEDKEY
title: TF_PRESERVEDKEY
author: windows-sdk-content
description: The TF_PRESERVEDKEY structure represents a preserved key.
old-location: tsf\tf_preservedkey.htm
old-project: TSF
ms.assetid: 95d37e94-3991-49c9-bddf-4183a69d49b9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TF_PRESERVEDKEY, TF_PRESERVEDKEY structure [Text Services Framework], _tsf_tf_preservedkey_ref, msctf/TF_PRESERVEDKEY, tsf.tf_preservedkey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_PRESERVEDKEY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msctf.h
api_name:
 - TF_PRESERVEDKEY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# TF_PRESERVEDKEY structure


## -description



The <b>TF_PRESERVEDKEY</b> structure represents a preserved key.




## -struct-fields




### -field uVKey

Virtual key code of the keyboard shortcut.


### -field uModifiers

Modifies the preserved key. This can be zero or a combination of one or more of the <a href="https://msdn.microsoft.com/4642ef17-34bd-4482-a9e9-0fbed7b574b1">TF_MOD_* constants</a>.


## -remarks



Preserved keys are registered by TSF text services and provide keyboard shortcuts to common commands implemented by the TSF text service.




## -see-also




<a href="https://msdn.microsoft.com/4642ef17-34bd-4482-a9e9-0fbed7b574b1">TF_MOD_* constants
      </a>
 

 

