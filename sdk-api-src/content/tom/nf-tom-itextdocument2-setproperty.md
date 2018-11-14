---
UID: NF:tom.ITextDocument2.SetProperty
title: ITextDocument2::SetProperty
author: windows-sdk-content
description: Specifies a new value for a property.
old-location: controls\itextdocument2_setproperty.htm
tech.root: controls
ms.assetid: 29e70a21-9fab-4fba-9cc4-f1268b005edb
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetProperty method, ITextDocument2.SetProperty, ITextDocument2::SetProperty, SetProperty, SetProperty method [Windows Controls], SetProperty method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_setproperty, tom/ITextDocument2::SetProperty
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
 - ITextDocument2.SetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tom.h
: 
- ITextDocument2.SetProperty
: 
---

# ITextDocument2::SetProperty


## -description


Specifies a new value for a property.


## -parameters




### -param Type [in]

Type: <b>long</b>

The identifier of the property. For a list of possible property identifiers, see <a href="https://msdn.microsoft.com/30775a51-0e63-453e-ac94-39d4510002f0"> GetProperty</a>.


### -param Value [in]

Type: <b>long</b>

The new property value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/30775a51-0e63-453e-ac94-39d4510002f0">ITextDocument2:: GetProperty</a>
 

 

