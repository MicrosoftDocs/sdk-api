---
UID: NN:iads.IADsComputerOperations
title: IADsComputerOperations (iads.h)
description: The IADsComputerOperations interface is a dual interface that inherits from IADs.
helpviewer_keywords: ["IADsComputerOperations","IADsComputerOperations interface [ADSI]","IADsComputerOperations interface [ADSI]","described","_ds_iadscomputeroperations","adsi.iadscomputeroperations","iads/IADsComputerOperations"]
old-location: adsi\iadscomputeroperations.htm
tech.root: adsi
ms.assetid: 9b0155ce-f313-43fa-8605-650aa8f38587
ms.date: 12/05/2018
ms.keywords: IADsComputerOperations, IADsComputerOperations interface [ADSI], IADsComputerOperations interface [ADSI],described, _ds_iadscomputeroperations, adsi.iadscomputeroperations, iads/IADsComputerOperations
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
 - IADsComputerOperations
 - iads/IADsComputerOperations
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
 - IADsComputerOperations
---

# IADsComputerOperations interface


## -description

The <b>IADsComputerOperations</b> interface is a dual interface that inherits from  <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It exposes methods for retrieving the status of a computer over a network and to enable remote shutdown. Directory service providers may choose to implement this interface to support basic system administration over a network through ADSI.

## -inheritance

The <b>IADsComputerOperations</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsComputerOperations</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscomputer">IADsComputer</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
