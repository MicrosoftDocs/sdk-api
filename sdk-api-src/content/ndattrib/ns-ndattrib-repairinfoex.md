---
UID: NS:ndattrib.tagRepairInfoEx
title: RepairInfoEx (ndattrib.h)
description: Contains detailed repair information that can be used to help resolve the root cause of an incident.
helpviewer_keywords: ["*PRepairInfoEx","PRepairInfoEx","PRepairInfoEx structure pointer [NDF]","RepairInfoEx","RepairInfoEx structure [NDF]","ndattrib/PRepairInfoEx","ndattrib/RepairInfoEx","ndf.repairinfoex"]
old-location: ndf\repairinfoex.htm
tech.root: NDF
ms.assetid: 9357f463-946c-47ad-bb8d-ff9de210e7e1
ms.date: 12/05/2018
ms.keywords: '*PRepairInfoEx, PRepairInfoEx, PRepairInfoEx structure pointer [NDF], RepairInfoEx, RepairInfoEx structure [NDF], ndattrib/PRepairInfoEx, ndattrib/RepairInfoEx, ndf.repairinfoex'
req.header: ndattrib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ndattrib.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RepairInfoEx, *PRepairInfoEx
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRepairInfoEx
 - ndattrib/tagRepairInfoEx
 - PRepairInfoEx
 - ndattrib/PRepairInfoEx
 - RepairInfoEx
 - ndattrib/RepairInfoEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndattrib.h
api_name:
 - RepairInfoEx
---

# RepairInfoEx structure


## -description

Contains detailed repair information that can be used to help resolve the  root cause of an incident.

## -struct-fields

### -field repair

Type: <b><a href="/windows/desktop/api/ndattrib/ns-ndattrib-repairinfo">RepairInfo</a></b>

The detailed repair information.

### -field repairRank

Type: <b>USHORT</b>

The rank of the repair, relative to other repairs in the <a href="/windows/desktop/api/ndattrib/ns-ndattrib-rootcauseinfo">RootCauseInfo</a> structure associated with the incident. A repair with rank 1 is expected to be more relevant to the problem and thus will be the first repair to be attempted. The success of any individual repair is not guaranteed, regardless of its rank.

## -see-also

<a href="/windows/desktop/NDF/freerepairinfoexs">FreeRepairInfoExs</a>



<a href="/windows/desktop/api/ndattrib/ns-ndattrib-repairinfo">RepairInfo</a>



<a href="/windows/desktop/api/ndattrib/ns-ndattrib-rootcauseinfo">RootCauseInfo</a>