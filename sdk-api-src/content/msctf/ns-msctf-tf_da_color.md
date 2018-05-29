---
UID: NS:msctf.TF_DA_COLOR
title: TF_DA_COLOR
author: windows-sdk-content
description: The TF_DA_COLOR structure contains color data used in the display attributes for a range of text.
old-location: tsf\tf_da_color.htm
old-project: TSF
ms.assetid: 0ce8f941-c187-437f-8bad-f882e63b8421
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: TF_DA_COLOR, TF_DA_COLOR structure [Text Services Framework], _tsf_tf_da_color_ref, msctf/TF_DA_COLOR, tsf.tf_da_color
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: TF_DA_COLOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Msctf.h
api_name:
-	TF_DA_COLOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# TF_DA_COLOR structure


## -description



The <b>TF_DA_COLOR</b> structure contains color data used in the display attributes for a range of text.




## -struct-fields




### -field type

Specifies the color type as defined in the <a href="https://msdn.microsoft.com/f692e188-d2f4-453b-a576-c6c05fd5f02a">TF_DA_COLORTYPE</a> enumeration.


### -field nIndex

Specifies the color as a system color index as defined in <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a>. This member is used only if <b>type</b> is equal to TF_CT_SYSCOLOR.


### -field cr

Specifies the color as an RGB value. This member is used only if <b>type</b> is equal to TF_CT_COLORREF.


## -see-also




<a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a>



<a href="https://msdn.microsoft.com/f692e188-d2f4-453b-a576-c6c05fd5f02a">TF_DA_COLORTYPE
      </a>
 

 

