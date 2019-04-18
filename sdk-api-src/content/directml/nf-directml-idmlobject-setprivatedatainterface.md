---
UID: NF:directml.IDMLObject.SetPrivateDataInterface
title: IDMLObject::SetPrivateDataInterface
author: windows-sdk-content
description: Associates an IUnknown-derived interface with the DirectML device object, and associates that interface with an application-defined GUID.
old-location: direct3d12\idmlobject_setprivatedatainterface.htm
tech.root: direct3d12
ms.assetid: 18D36A5A-07C4-4926-8B31-BBB75EAEC6A9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDMLObject interface,SetPrivateDataInterface method, IDMLObject.SetPrivateDataInterface, IDMLObject::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method, SetPrivateDataInterface method,IDMLObject interface, direct3d12.idmlobject_setprivatedatainterface, directml/IDMLObject::SetPrivateDataInterface
ms.topic: method
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.dll
api_name:
 - IDMLObject.SetPrivateDataInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLObject::SetPrivateDataInterface


## -description






Associates an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>-derived interface with the DirectML device object, and associates that interface with an application-defined <b>GUID</b>.


## -parameters




### -param guid [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/cc237815(PROT.13).aspx">REFGUID</a></b>

The <b>GUID</b> to associate with the interface.


### -param data [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>-derived interface to be associated with the device object.


## -returns



Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.




## -see-also




[IDMLObject](/windows/desktop/api/directml/nn-directml-idmlobject)
 

 

