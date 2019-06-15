---
UID: NN:propsys.ICreateObject
title: ICreateObject (propsys.h)
author: windows-sdk-content
description: Exposes a method that creates an object of a specified class.
old-location: shell\ICreateObject.htm
tech.root: shell
ms.assetid: 90502b4a-dc0a-4077-83d7-e9f5445ba69b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICreateObject, ICreateObject interface [Windows Shell], ICreateObject interface [Windows Shell],described, _shell_ICreateObject, propsys/ICreateObject, shell.ICreateObject
ms.topic: interface
f1_keywords: ["propsys/ICreateObject"]
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - COM
api_location:
 - Propsys.h
api_name:
 - ICreateObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICreateObject interface


## -description


Exposes a method that creates an object of a specified class.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICreateObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-icreateobject-createobject">CreateObject</a>
</td>
<td align="left" width="63%">
Creates a local object of a specified class and returns a pointer to a specified interface on the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystorewithcreateobject">IShellItem2::GetPropertyStoreWithCreateObject</a>
 

 

