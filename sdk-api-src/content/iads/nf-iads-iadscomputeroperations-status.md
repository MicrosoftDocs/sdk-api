---
UID: NF:iads.IADsComputerOperations.Status
title: IADsComputerOperations::Status (iads.h)

description: The IADsComputerOperations::Status method retrieves the status of a computer.
old-location: adsi\iadscomputeroperations_status.htm
tech.root: adsi
ms.assetid: 85243a67-3fe4-43f2-8173-4e9a507609ba

ms.date: 12/05/2018
ms.keywords: IADsComputerOperations interface [ADSI],Status method, IADsComputerOperations.Status, IADsComputerOperations::Status, Status, Status method [ADSI], Status method [ADSI],IADsComputerOperations interface, _ds_iadscomputeroperations_status, adsi.iadscomputeroperations__status, adsi.iadscomputeroperations_status, iads/IADsComputerOperations::Status
ms.topic: method
f1_keywords: 
 - "iads/IADsComputerOperations.Status"
dev_langs:
 - c++
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
 - IADsComputerOperations.Status
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsComputerOperations::Status


## -description


The <b>IADsComputerOperations::Status</b> method retrieves the status of a computer.


## -parameters




### -param ppObject [out]

Pointer to an  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface that reports the status code of computer operations. The status code is provider-specific.


## -returns



This method supports the standard return values as well as the following:

For other return values, see  <a href="https://docs.microsoft.com/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadscomputer">IADsComputer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadscomputeroperations">IADsComputerOperations</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

