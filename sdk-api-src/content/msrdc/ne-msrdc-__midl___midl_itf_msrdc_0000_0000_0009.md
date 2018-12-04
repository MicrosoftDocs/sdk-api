---
UID: NE:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0009
title: "__MIDL___MIDL_itf_msrdc_0000_0000_0009"
author: windows-sdk-content
description: Defines values that describe the state of the similarity traits table, similarity file ID table, or both.
old-location: rdc\rdccreatedtables.htm
tech.root: rdc
ms.assetid: f46dd0f0-22b0-41fb-a7c2-29d1b4514f7e
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: RDCTABLE_Existing, RDCTABLE_InvalidOrUnknown, RDCTABLE_New, RdcCreatedTables, RdcCreatedTables enumeration [Remote Differential Compression], __MIDL___MIDL_itf_msrdc_0000_0000_0009, fs.rdccreatedtables, msrdc/RDCTABLE_Existing, msrdc/RDCTABLE_InvalidOrUnknown, msrdc/RDCTABLE_New, msrdc/RdcCreatedTables, rdc.rdccreatedtables
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MsRdc.h
api_name:
 - RdcCreatedTables
product: Windows
targetos: Windows
req.typenames: RdcCreatedTables
req.redist: 
---

# __MIDL___MIDL_itf_msrdc_0000_0000_0009 enumeration


## -description


Defines values that describe the state of the similarity traits table, similarity file ID table, or both.


## -enum-fields




### -field RDCTABLE_InvalidOrUnknown

The table contains data that is not valid.


### -field RDCTABLE_Existing

The table is an existing table.


### -field RDCTABLE_New

The table is a new table.


## -see-also




<a href="https://msdn.microsoft.com/808c20f9-054d-475d-8ca3-ee2dde871426">ISimilarity::CreateTable</a>



<a href="https://msdn.microsoft.com/bc683c53-5491-4cc6-abe1-c82e69aaa7f4">ISimilarityFileIdTable::CreateTable</a>



<a href="https://msdn.microsoft.com/35fd9ea1-85bf-424c-b0e2-dcdfbb6940fb">ISimilarityTraitsTable::CreateTable</a>
 

 

