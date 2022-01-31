---
UID: NE:sdoias._IASDATASTORE
title: IASDATASTORE (sdoias.h)
description: The values of the IASDATASTORE enumeration indicate the possible storage locations for SDO data.
helpviewer_keywords: ["*PIASDATASTORE","DATA_STORE_DIRECTORY","DATA_STORE_LOCAL","IASDATASTORE","IASDATASTORE enumeration [Network Policy Server]","PIASDATASTORE","PIASDATASTORE enumeration pointer [Network Policy Server]","_sdo_iasdatastore","nps.SDO_iasdatastore","sdo.iasdatastore","sdoias/DATA_STORE_DIRECTORY","sdoias/DATA_STORE_LOCAL","sdoias/IASDATASTORE","sdoias/PIASDATASTORE"]
old-location: nps\SDO_iasdatastore.htm
tech.root: Nps
ms.assetid: 1eec69f9-b82e-48e5-a471-0a0626d91957
ms.date: 12/05/2018
ms.keywords: '*PIASDATASTORE, DATA_STORE_DIRECTORY, DATA_STORE_LOCAL, IASDATASTORE, IASDATASTORE enumeration [Network Policy Server], PIASDATASTORE, PIASDATASTORE enumeration pointer [Network Policy Server], _sdo_iasdatastore, nps.SDO_iasdatastore, sdo.iasdatastore, sdoias/DATA_STORE_DIRECTORY, sdoias/DATA_STORE_LOCAL, sdoias/IASDATASTORE, sdoias/PIASDATASTORE'
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IASDATASTORE, *PIASDATASTORE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IASDATASTORE
 - sdoias/_IASDATASTORE
 - PIASDATASTORE
 - sdoias/PIASDATASTORE
 - IASDATASTORE
 - sdoias/IASDATASTORE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - IASDATASTORE
---

# IASDATASTORE enumeration


## -description

The values of the 
<b>IASDATASTORE</b> enumeration indicate the possible storage locations for SDO data.

## -enum-fields

### -field DATA_STORE_LOCAL:0

The SDO data is stored locally on the SDO computer.

### -field DATA_STORE_DIRECTORY

The SDO data is stored in the Active Directory.

## -remarks

You cannot use this enumeration type to specify the storage location for SDO data.

## -see-also

<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo">ISdoMachine::GetServiceSDO</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo">ISdoMachine::GetUserSDO</a>
