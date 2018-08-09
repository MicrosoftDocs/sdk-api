---
UID: NE:sdoias._IASDATASTORE
title: "_IASDATASTORE"
author: windows-sdk-content
description: The values of the IASDATASTORE enumeration indicate the possible storage locations for SDO data.
old-location: nps\SDO_iasdatastore.htm
old-project: nps
ms.assetid: 1eec69f9-b82e-48e5-a471-0a0626d91957
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PIASDATASTORE, DATA_STORE_DIRECTORY, DATA_STORE_LOCAL, IASDATASTORE, IASDATASTORE enumeration [Network Policy Server], PIASDATASTORE, PIASDATASTORE enumeration pointer [Network Policy Server], _IASDATASTORE, _sdo_iasdatastore, nps.SDO_iasdatastore, sdo.iasdatastore, sdoias/DATA_STORE_DIRECTORY, sdoias/DATA_STORE_LOCAL, sdoias/IASDATASTORE, sdoias/PIASDATASTORE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ConvertStringSidToSidW (Unicode) and ConvertStringSidToSidA (ANSI)
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IASDATASTORE, *PIASDATASTORE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - IASDATASTORE
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# _IASDATASTORE enumeration


## -description


The values of the 
<b>IASDATASTORE</b> enumeration indicate the possible storage locations for SDO data.


## -enum-fields




### -field DATA_STORE_LOCAL

The SDO data is stored locally on the SDO computer.


### -field DATA_STORE_DIRECTORY

The SDO data is stored in the Active Directory.


## -remarks



You cannot use this enumeration type to specify the storage location for SDO data.




## -see-also




<a href="https://msdn.microsoft.com/265f034a-78be-4792-958e-80ad7a71d1a7">ISdoMachine::GetServiceSDO</a>



<a href="https://msdn.microsoft.com/c416c0db-836a-4056-bcd7-819f10923446">ISdoMachine::GetUserSDO</a>
 

 

