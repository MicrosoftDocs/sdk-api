---
UID: NS:mssip.MS_ADDINFO_FLAT_
title: MS_ADDINFO_FLAT_
author: windows-sdk-content
description: Provides additional information about flat or end-to-end subject types.
old-location: security\ms_addinfo_flat.htm
tech.root: seccrypto
ms.assetid: 9f5bebd1-8eda-456d-9339-3334a19c0ea4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PMS_ADDINFO_FLAT, MS_ADDINFO_FLAT, MS_ADDINFO_FLAT structure [Security], MS_ADDINFO_FLAT_, PMS_ADDINFO_FLAT, PMS_ADDINFO_FLAT structure pointer [Security], mssip/MS_ADDINFO_FLAT_, mssip/PMS_ADDINFO_FLAT, security.ms_addinfo_flat"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mssip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mssip.h
api_name:
 - MS_ADDINFO_FLAT
product: Windows
targetos: Windows
req.typenames: MS_ADDINFO_FLAT, *PMS_ADDINFO_FLAT
req.redist: 
---

# MS_ADDINFO_FLAT_ structure


## -description


The <b>MS_ADDINFO_FLAT</b> structure provides additional information about flat or end-to-end subject types.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field pIndirectData

A <a href="https://msdn.microsoft.com/d34b599b-fe49-47c4-bb52-73ee14d73253">SIP_INDIRECT_DATA</a> structure that contains the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of a flat file subject.

