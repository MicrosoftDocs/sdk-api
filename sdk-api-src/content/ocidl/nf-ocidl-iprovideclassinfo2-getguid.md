---
UID: NF:ocidl.IProvideClassInfo2.GetGUID
title: IProvideClassInfo2::GetGUID
author: windows-sdk-content
description: Retrieves the specified GUID for the object.
old-location: com\iprovideclassinfo2_getguid.htm
tech.root: com
ms.assetid: 1a424b93-93a9-4dc7-9c77-349522ee9e70
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetGUID, GetGUID method [COM], GetGUID method [COM],IProvideClassInfo2 interface, IProvideClassInfo2 interface [COM],GetGUID method, IProvideClassInfo2.GetGUID, IProvideClassInfo2::GetGUID, _com_iprovideclassinfo2_getguid, com.iprovideclassinfo2_getguid, ocidl/IProvideClassInfo2::GetGUID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - OCIdl.h
api_name:
 - IProvideClassInfo2.GetGUID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProvideClassInfo2::GetGUID


## -description


Retrieves the specified GUID for the object.


## -parameters




### -param dwGuidKind [in]

The GUID type. Possible values are from the <a href="https://msdn.microsoft.com/b9ddd96b-0418-4e31-aaf9-ca060c405fa7">GUIDKIND</a> enumeration.


### -param pGUID [out]

A pointer to a variable that receives the GUID.


## -returns



This method can return the standard return values E_INVALIDARG, E_UNEXPECTED, E_POINTER, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/e62785e4-994c-48cc-b5b9-7ec2b07c9d63">IProvideClassInfo2</a>
 

 

