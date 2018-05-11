---
UID: NE:msctf.__MIDL___MIDL_itf_msctf_0000_0070_0004
title: "__MIDL___MIDL_itf_msctf_0000_0070_0004"
author: windows-driver-content
description: Elements of the TF_DA_ATTR_INFO enumeration are used to specify text conversion data in the TF_DISPLAYATTRIBUTE structure.
old-location: tsf\tf_da_attr_info.htm
old-project: TSF
ms.assetid: 894e6c15-d911-4e0c-96b1-db6ec8e43eba
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: TF_ATTR_CONVERTED, TF_ATTR_FIXEDCONVERTED, TF_ATTR_INPUT, TF_ATTR_INPUT_ERROR, TF_ATTR_OTHER, TF_ATTR_TARGET_CONVERTED, TF_ATTR_TARGET_NOTCONVERTED, TF_DA_ATTR_INFO, TF_DA_ATTR_INFO enumeration [Text Services Framework], __MIDL___MIDL_itf_msctf_0000_0070_0004, _tsf_tf_da_attr_info_ref, msctf/TF_ATTR_CONVERTED, msctf/TF_ATTR_FIXEDCONVERTED, msctf/TF_ATTR_INPUT, msctf/TF_ATTR_INPUT_ERROR, msctf/TF_ATTR_OTHER, msctf/TF_ATTR_TARGET_CONVERTED, msctf/TF_ATTR_TARGET_NOTCONVERTED, msctf/TF_DA_ATTR_INFO, tsf.tf_da_attr_info
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.type-library: MsClus.tlb
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Msctf.h
api_name:
-	TF_DA_ATTR_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_msctf_0000_0070_0004 enumeration


## -description


Elements of the <b>TF_DA_ATTR_INFO</b> enumeration are used to specify text conversion data in the <a href="https://msdn.microsoft.com/29faaa22-ea03-4a2e-a035-7979e2a89fc9">TF_DISPLAYATTRIBUTE</a> structure.


## -enum-fields




### -field TF_ATTR_INPUT

The text is entered by the user and has not been converted yet.


### -field TF_ATTR_TARGET_CONVERTED

The user has made a character selection and the text has been converted yet.


### -field TF_ATTR_CONVERTED

The text is converted.


### -field TF_ATTR_TARGET_NOTCONVERTED

The user made a character selection, but the text is not converted yet.


### -field TF_ATTR_INPUT_ERROR

The text is an error character and cannot be converted. For example, some consonants cannot be put together.


### -field TF_ATTR_FIXEDCONVERTED

The text is not converted. Theses characters will no longer be converted.


### -field TF_ATTR_OTHER

Reserved for the system.


## -see-also




<a href="https://msdn.microsoft.com/29faaa22-ea03-4a2e-a035-7979e2a89fc9">TF_DISPLAYATTRIBUTE
      </a>
 

 

