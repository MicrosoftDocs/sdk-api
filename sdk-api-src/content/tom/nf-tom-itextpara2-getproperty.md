---
UID: NF:tom.ITextPara2.GetProperty
title: ITextPara2::GetProperty
author: windows-sdk-content
description: Gets the value of the specified property.
old-location: controls\itextpara2_getproperty.htm
tech.root: Controls
ms.assetid: 628ec2d7-2553-4a76-a5e6-c3a5bef3f8d6
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetProperty, GetProperty method [Windows Controls], GetProperty method [Windows Controls],ITextPara2 interface, ITextPara2 interface [Windows Controls],GetProperty method, ITextPara2.GetProperty, ITextPara2::GetProperty, controls.itextpara2_getproperty, tom/ITextPara2::GetProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextPara2.GetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara2::GetProperty


## -description


Gets the value of the specified property.


## -parameters




### -param Type [in]

Type: <b>long</b>

The ID of the property value to retrieve.


### -param pValue [out]

Type: <b>long*</b>

The property value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The <a href="tomconstants.htm">tomParaPropMathAlign</a> property sets the math alignment for math paragraphs in a text paragraph. It can have one of the following values.<dl>
<dd><a href="tomconstants.htm">tomMathParaAlignDefault</a></dd>
<dd><a href="tomconstants.htm">tomMathParaAlignCenterGroup</a></dd>
<dd><a href="tomconstants.htm">tomMathParaAlignCenter</a></dd>
<dd><a href="tomconstants.htm">tomMathParaAlignLeft</a></dd>
<dd><a href="tomconstants.htm">tomMathParaAlignRight</a></dd>
</dl>





## -see-also




<a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>



<a href="https://msdn.microsoft.com/5a95c055-5118-4c2a-8f63-3a2a3114451e">ITextPara2::SetProperty</a>
 

 

