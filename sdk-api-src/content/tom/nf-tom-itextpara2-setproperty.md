---
UID: NF:tom.ITextPara2.SetProperty
title: ITextPara2::SetProperty
author: windows-sdk-content
description: Sets the property value.
old-location: controls\itextpara2_setproperty.htm
tech.root: controls
ms.assetid: 5a95c055-5118-4c2a-8f63-3a2a3114451e
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ITextPara2 interface [Windows Controls],SetProperty method, ITextPara2.SetProperty, ITextPara2::SetProperty, SetProperty, SetProperty method [Windows Controls], SetProperty method [Windows Controls],ITextPara2 interface, controls.itextpara2_setproperty, tom/ITextPara2::SetProperty
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
 - ITextPara2.SetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara2::SetProperty


## -description


Sets the property value.


## -parameters




### -param Type [in]

Type: <b>long</b>

The property ID of the property value to set. See <a href="https://msdn.microsoft.com/628ec2d7-2553-4a76-a5e6-c3a5bef3f8d6">ITextPara2::GetProperty</a> for a list of defined properties.


### -param Value [in]

Type: <b>long</b>

The property value to set.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>



<a href="https://msdn.microsoft.com/628ec2d7-2553-4a76-a5e6-c3a5bef3f8d6">ITextPara2::GetProperty</a>
 

 

