---
UID: NF:sdoias.ISdoMachine.IsDirectoryAvailable
title: ISdoMachine::IsDirectoryAvailable (sdoias.h)
description: The IsDirectoryAvailable method tests whether an Active Directory service is available on the SDO computer.
helpviewer_keywords: ["ISdoMachine interface [Network Policy Server]","IsDirectoryAvailable method","ISdoMachine.IsDirectoryAvailable","ISdoMachine::IsDirectoryAvailable","IsDirectoryAvailable","IsDirectoryAvailable method [Network Policy Server]","IsDirectoryAvailable method [Network Policy Server]","ISdoMachine interface","IsDirectoryAvailable method [Network Policy Server]","SdoMachine object","SdoMachine object [Network Policy Server]","IsDirectoryAvailable method","_sdo_isdomachine_isdirectoryavailable","nps.SDO_isdomachine_isdirectoryavailable","sdo.isdomachine_isdirectoryavailable","sdoias/ISdoMachine::IsDirectoryAvailable"]
old-location: nps\SDO_isdomachine_isdirectoryavailable.htm
tech.root: Nps
ms.assetid: 733d2911-7e1d-4f73-ae24-1bb748213c1c
ms.date: 12/05/2018
ms.keywords: ISdoMachine interface [Network Policy Server],IsDirectoryAvailable method, ISdoMachine.IsDirectoryAvailable, ISdoMachine::IsDirectoryAvailable, IsDirectoryAvailable, IsDirectoryAvailable method [Network Policy Server], IsDirectoryAvailable method [Network Policy Server],ISdoMachine interface, IsDirectoryAvailable method [Network Policy Server],SdoMachine object, SdoMachine object [Network Policy Server],IsDirectoryAvailable method, _sdo_isdomachine_isdirectoryavailable, nps.SDO_isdomachine_isdirectoryavailable, sdo.isdomachine_isdirectoryavailable, sdoias/ISdoMachine::IsDirectoryAvailable
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Iassdo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISdoMachine::IsDirectoryAvailable
 - sdoias/ISdoMachine::IsDirectoryAvailable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoMachine.IsDirectoryAvailable
 - SdoMachine.IsDirectoryAvailable
---

# ISdoMachine::IsDirectoryAvailable


## -description

The 
<b>IsDirectoryAvailable</b> method tests whether an Active Directory service is available on the SDO computer.

## -parameters

### -param boolDirectoryAvailable [out]

Specifies whether the Active Directory is available. If the Active Directory is available, this parameter is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -remarks

Before calling this method, use the 
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">ISdoMachine::Attach</a> method to attach to the SDO computer.

<div class="alert"><b>Important</b>  Always returns <b>VARIANT_FALSE</b> in the current implementation.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/sdoias/nn-sdoias-isdomachine">ISdoMachine</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">ISdoMachine::Attach</a>