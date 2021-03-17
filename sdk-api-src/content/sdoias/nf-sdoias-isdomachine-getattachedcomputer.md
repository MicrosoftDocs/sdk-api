---
UID: NF:sdoias.ISdoMachine.GetAttachedComputer
title: ISdoMachine::GetAttachedComputer (sdoias.h)
description: The GetAttachedComputer method retrieves the name of the computer that is currently attached as an SDO computer.
helpviewer_keywords: ["GetAttachedComputer","GetAttachedComputer method [Network Policy Server]","GetAttachedComputer method [Network Policy Server]","ISdoMachine interface","GetAttachedComputer method [Network Policy Server]","SdoMachine object","ISdoMachine interface [Network Policy Server]","GetAttachedComputer method","ISdoMachine.GetAttachedComputer","ISdoMachine::GetAttachedComputer","SdoMachine object [Network Policy Server]","GetAttachedComputer method","_sdo_isdomachine_getattachedcomputer","nps.SDO_isdomachine_getattachedcomputer","sdo.isdomachine_getattachedcomputer","sdoias/ISdoMachine::GetAttachedComputer"]
old-location: nps\SDO_isdomachine_getattachedcomputer.htm
tech.root: Nps
ms.assetid: ac2fe3e3-a1cb-4642-90af-2b0203e29251
ms.date: 12/05/2018
ms.keywords: GetAttachedComputer, GetAttachedComputer method [Network Policy Server], GetAttachedComputer method [Network Policy Server],ISdoMachine interface, GetAttachedComputer method [Network Policy Server],SdoMachine object, ISdoMachine interface [Network Policy Server],GetAttachedComputer method, ISdoMachine.GetAttachedComputer, ISdoMachine::GetAttachedComputer, SdoMachine object [Network Policy Server],GetAttachedComputer method, _sdo_isdomachine_getattachedcomputer, nps.SDO_isdomachine_getattachedcomputer, sdo.isdomachine_getattachedcomputer, sdoias/ISdoMachine::GetAttachedComputer
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
 - ISdoMachine::GetAttachedComputer
 - sdoias/ISdoMachine::GetAttachedComputer
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
 - ISdoMachine.GetAttachedComputer
 - SdoMachine.GetAttachedComputer
---

# ISdoMachine::GetAttachedComputer


## -description

The <b>GetAttachedComputer</b> method 
    retrieves the name of the computer that is currently attached as an SDO computer.

## -parameters

### -param bstrComputerName [out]

Pointer to a <a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> that 
      receives the name of the computer that is the currently-attached SDO computer.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If no computer is currently attached, the return value is <b>E_FAIL</b>.

The method may also return one of the following error codes.

## -remarks

The <b>GetAttachedComputer</b> allocates 
    the memory for the <a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> 
    variable. The calling application should free this memory by calling 
    <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

## -see-also

<a href="/windows/desktop/api/sdoias/nn-sdoias-isdomachine">ISdoMachine</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">ISdoMachine::Attach</a>