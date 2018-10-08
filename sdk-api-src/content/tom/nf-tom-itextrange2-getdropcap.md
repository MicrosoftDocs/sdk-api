---
UID: NF:tom.ITextRange2.GetDropCap
title: ITextRange2::GetDropCap
author: windows-sdk-content
description: Gets the drop-cap parameters of the paragraph that contains this range.
old-location: controls\itextrange2_getdropcap.htm
tech.root: controls
ms.assetid: c653c002-6708-4813-83ae-1ea578bdcee2
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetDropCap, GetDropCap method [Windows Controls], GetDropCap method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetDropCap method, ITextRange2.GetDropCap, ITextRange2::GetDropCap, controls.itextrange2_getdropcap, tom/ITextRange2::GetDropCap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: Tom.h
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
 - ITextRange2.GetDropCap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange2::GetDropCap


## -description


Not implemented.

Gets the drop-cap parameters of the paragraph that contains this range.


## -parameters




### -param pcLine [out]

Type: <b>long*</b>

The count of lines for the drop cap.  A value of 0 means no drop cap.


### -param pPosition [out]

Type: <b>long*</b>

The position of the drop cap. The position can be one of the following: 

<ul>
<li>tomDropMargin</li>
<li>tomDropNone</li>
<li>tomDropNormal</li>
</ul>

## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>



<a href="https://msdn.microsoft.com/189c1a69-44eb-4de0-8ffc-9a026d9e6f16">ITextRange2::SetDropCap</a>
 

 

