---
UID: NF:sdoias.ISdoMachine.GetOSType
title: ISdoMachine::GetOSType (sdoias.h)
description: The GetOSType method retrieves the type of operating system running on the SDO computer.
old-location: nps\SDO_isdomachine_getostype.htm
tech.root: Nps
ms.assetid: aa4f31af-57b0-4ce2-b8b9-981e4ef30d31
ms.date: 12/05/2018
ms.keywords: GetOSType, GetOSType method [Network Policy Server], GetOSType method [Network Policy Server],ISdoMachine interface, GetOSType method [Network Policy Server],SdoMachine object, ISdoMachine interface [Network Policy Server],GetOSType method, ISdoMachine.GetOSType, ISdoMachine::GetOSType, SdoMachine object [Network Policy Server],GetOSType method, _sdo_isdomachine_getostype, nps.SDO_isdomachine_getostype, sdo.isdomachine_getostype, sdoias/ISdoMachine::GetOSType
f1_keywords:
- sdoias/ISdoMachine.GetOSType
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Iassdo.dll
api_name:
- ISdoMachine.GetOSType
- SdoMachine.GetOSType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISdoMachine::GetOSType


## -description


The 
<b>GetOSType</b> method retrieves the type of operating system running on the SDO computer.


## -parameters




### -param eOSType [out]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/ne-sdoias-iasostype">IASOSTYPE</a> variable that receives the type of the operating system on the SDO computer.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Before calling this method, use the 
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">ISdoMachine::Attach</a> method to attach to the SDO computer.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/ne-sdoias-iasostype">IASOSTYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nn-sdoias-isdomachine">ISdoMachine</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">ISdoMachine::Attach</a>
 

 

