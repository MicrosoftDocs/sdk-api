---
UID: NF:iads.IADsContainer.CopyHere
title: IADsContainer::CopyHere
author: windows-sdk-content
description: The IADsContainer::CopyHere method creates a copy of the specified directory object in this container.
old-location: adsi\iadscontainer_copyhere.htm
tech.root: ADSI
ms.assetid: 8a006253-ccb4-4f13-93b5-297db17f7c2e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CopyHere, CopyHere method [ADSI], CopyHere method [ADSI],IADsContainer interface, IADsContainer interface [ADSI],CopyHere method, IADsContainer.CopyHere, IADsContainer::CopyHere, _ds_iadscontainer_copyhere, adsi.iadscontainer__copyhere, adsi.iadscontainer_copyhere, iads/IADsContainer::CopyHere
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsContainer.CopyHere
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsContainer::CopyHere


## -description


The <b>IADsContainer::CopyHere</b> method creates a  copy of the specified directory object in this container.


## -parameters




### -param SourceName

TBD


### -param NewName

TBD


### -param ppObject

TBD




#### - bstrNewName [in]

Optional name of the new object within the container. If a new name is not specified  for the object, set to <b>NULL</b>; the new object will have the same name as the source object.


#### - bstrSourceObject [in]

The ADsPath of the object to copy.


#### - ppNewObject [out]

Indirect pointer to the  <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a> interface on the copied object.


## -returns



This method supports the standard return values, including <b>S_OK</b> for a successful operation. For more information and  error code information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The destination container must be in the same directory service as the source container. An object cannot be copied across a directory service implementation.

The  providers supplied with ADSI return the <b>E_NOTIMPL</b> error message.




## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="https://msdn.microsoft.com/132b1cdc-6fb5-43b1-a5de-3b25c361e8e1">IADsContainer::MoveHere</a>
 

 

