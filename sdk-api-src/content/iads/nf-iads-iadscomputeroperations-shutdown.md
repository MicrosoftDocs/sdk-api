---
UID: NF:iads.IADsComputerOperations.Shutdown
title: IADsComputerOperations::Shutdown (iads.h)
description: The IADsComputerOperations::Shutdown method causes a computer under ADSI control to execute the shutdown operation with an optional reboot.
helpviewer_keywords: ["IADsComputerOperations interface [ADSI]","Shutdown method","IADsComputerOperations.Shutdown","IADsComputerOperations::Shutdown","Shutdown","Shutdown method [ADSI]","Shutdown method [ADSI]","IADsComputerOperations interface","_ds_iadscomputeroperations_shutdown","adsi.iadscomputeroperations__shutdown","adsi.iadscomputeroperations_shutdown","iads/IADsComputerOperations::Shutdown"]
old-location: adsi\iadscomputeroperations_shutdown.htm
tech.root: adsi
ms.assetid: b13502d6-11eb-406b-bed0-e9d14e61e424
ms.date: 12/05/2018
ms.keywords: IADsComputerOperations interface [ADSI],Shutdown method, IADsComputerOperations.Shutdown, IADsComputerOperations::Shutdown, Shutdown, Shutdown method [ADSI], Shutdown method [ADSI],IADsComputerOperations interface, _ds_iadscomputeroperations_shutdown, adsi.iadscomputeroperations__shutdown, adsi.iadscomputeroperations_shutdown, iads/IADsComputerOperations::Shutdown
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
 - IADsComputerOperations::Shutdown
 - iads/IADsComputerOperations::Shutdown
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
 - IADsComputerOperations.Shutdown
---

# IADsComputerOperations::Shutdown


## -description

The <b>IADsComputerOperations::Shutdown</b> method causes a computer under ADSI control to execute the shutdown operation with an optional reboot.

## -parameters

### -param bReboot [in]

If <b>TRUE</b>, then reboot the computer after the shutdown is complete.

## -returns

This method supports the standard return values, as well as the following:

For other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadscomputer">IADsComputer</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscomputeroperations">IADsComputerOperations</a>