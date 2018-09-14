---
UID: NE:msctf.__MIDL___MIDL_itf_msctf_0000_0070_0002
title: "__MIDL___MIDL_itf_msctf_0000_0070_0002"
author: windows-sdk-content
description: Elements of the TF_DA_COLORTYPE enumeration specify the format of the color contained in the TF_DA_COLOR structure.
old-location: tsf\tf_da_colortype.htm
tech.root: TSF
ms.assetid: f692e188-d2f4-453b-a576-c6c05fd5f02a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: TF_CT_COLORREF, TF_CT_NONE, TF_CT_SYSCOLOR, TF_DA_COLORTYPE, TF_DA_COLORTYPE enumeration [Text Services Framework], __MIDL___MIDL_itf_msctf_0000_0070_0002, _tsf_tf_da_colortype_ref, msctf/TF_CT_COLORREF, msctf/TF_CT_NONE, msctf/TF_CT_SYSCOLOR, msctf/TF_DA_COLORTYPE, tsf.tf_da_colortype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msctf.h
api_name:
 - TF_DA_COLORTYPE
product: Windows
targetos: Windows
req.typenames: TF_DA_COLORTYPE
req.redist: TSF 1.0 on Windows 2000 Professional
---

# __MIDL___MIDL_itf_msctf_0000_0070_0002 enumeration


## -description


Elements of the <b>TF_DA_COLORTYPE</b> enumeration specify the format of the color contained in the <a href="https://msdn.microsoft.com/0ce8f941-c187-437f-8bad-f882e63b8421">TF_DA_COLOR</a> structure.


## -enum-fields




### -field TF_CT_NONE

The structure contains no color data.


### -field TF_CT_SYSCOLOR

The color is specified as a system color index. For more information about the system color indexes, see <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a>.


### -field TF_CT_COLORREF

The color is specified as an RGB value.


## -see-also




<a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a>



<a href="https://msdn.microsoft.com/0ce8f941-c187-437f-8bad-f882e63b8421">TF_DA_COLOR
      </a>
 

 

