---
UID: NF:iads.IADsContainer.CopyHere
title: IADsContainer::CopyHere (iads.h)
description: The IADsContainer::CopyHere method creates a copy of the specified directory object in this container.
helpviewer_keywords: ["CopyHere","CopyHere method [ADSI]","CopyHere method [ADSI]","IADsContainer interface","IADsContainer interface [ADSI]","CopyHere method","IADsContainer.CopyHere","IADsContainer::CopyHere","_ds_iadscontainer_copyhere","adsi.iadscontainer__copyhere","adsi.iadscontainer_copyhere","iads/IADsContainer::CopyHere"]
old-location: adsi\iadscontainer_copyhere.htm
tech.root: adsi
ms.assetid: 8a006253-ccb4-4f13-93b5-297db17f7c2e
ms.date: 12/05/2018
ms.keywords: CopyHere, CopyHere method [ADSI], CopyHere method [ADSI],IADsContainer interface, IADsContainer interface [ADSI],CopyHere method, IADsContainer.CopyHere, IADsContainer::CopyHere, _ds_iadscontainer_copyhere, adsi.iadscontainer__copyhere, adsi.iadscontainer_copyhere, iads/IADsContainer::CopyHere
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsContainer::CopyHere
 - iads/IADsContainer::CopyHere
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsContainer.CopyHere
---

# IADsContainer::CopyHere


## -description

The <b>IADsContainer::CopyHere</b> method creates a  copy of the specified directory object in this container.

## -parameters

### -param SourceName [in]

The ADsPath of the object to copy.

### -param NewName [in]

Optional name of the new object within the container. If a new name is not specified  for the object, set to <b>NULL</b>; the new object will have the same name as the source object.

### -param ppObject [out]

Indirect pointer to the  <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a> interface on the copied object.

## -returns

This method supports the standard return values, including <b>S_OK</b> for a successful operation. For more information and  error code information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The destination container must be in the same directory service as the source container. An object cannot be copied across a directory service implementation.

The  providers supplied with ADSI return the <b>E_NOTIMPL</b> error message.

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/windows/desktop/api/iads/nf-iads-iadscontainer-movehere">IADsContainer::MoveHere</a>