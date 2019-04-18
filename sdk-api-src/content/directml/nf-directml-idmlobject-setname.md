---
UID: NF:directml.IDMLObject.SetName
title: IDMLObject::SetName
author: windows-sdk-content
description: Associates a name with the DirectML device object. This name is for use in debug diagnostics and tools.
old-location: direct3d12\idmlobject_setname.htm
tech.root: direct3d12
ms.assetid: DD74B028-74EF-4D76-81A7-F150302F80D2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDMLObject interface,SetName method, IDMLObject.SetName, IDMLObject::SetName, SetName, SetName method, SetName method,IDMLObject interface, direct3d12.idmlobject_setname, directml/IDMLObject::SetName
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
 - IDMLObject.SetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLObject::SetName


## -description






Associates a name with the DirectML device object.
          This name is for use in debug diagnostics and tools.
        


## -parameters




### -param name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PCWSTR</a></b>

A <b>NULL</b>-terminated <b>UNICODE</b> string that contains the name to associate with the DirectML device object.
          


## -returns



Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.




## -see-also




[IDMLObject](/windows/desktop/api/directml/nn-directml-idmlobject)
 

 

