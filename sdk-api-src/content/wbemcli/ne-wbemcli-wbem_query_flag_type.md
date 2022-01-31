---
UID: NE:wbemcli.tag_WBEM_QUERY_FLAG_TYPE
title: WBEM_QUERY_FLAG_TYPE (wbemcli.h)
description: Contains flags used to define a query or enumerator.
helpviewer_keywords: ["WBEM_FLAG_DEEP","WBEM_FLAG_PROTOTYPE","WBEM_FLAG_SHALLOW","WBEM_QUERY_FLAG_TYPE","WBEM_QUERY_FLAG_TYPE enumeration [Windows Management Instrumentation]","wbemcli/WBEM_FLAG_DEEP","wbemcli/WBEM_FLAG_PROTOTYPE","wbemcli/WBEM_FLAG_SHALLOW","wbemcli/WBEM_QUERY_FLAG_TYPE","wmi.wbem_query_flag_type"]
old-location: wmi\wbem_query_flag_type.htm
tech.root: wmi
ms.assetid: D0F53F94-682A-432D-8FBA-8EC05C6B69BF
ms.date: 12/05/2018
ms.keywords: WBEM_FLAG_DEEP, WBEM_FLAG_PROTOTYPE, WBEM_FLAG_SHALLOW, WBEM_QUERY_FLAG_TYPE, WBEM_QUERY_FLAG_TYPE enumeration [Windows Management Instrumentation], wbemcli/WBEM_FLAG_DEEP, wbemcli/WBEM_FLAG_PROTOTYPE, wbemcli/WBEM_FLAG_SHALLOW, wbemcli/WBEM_QUERY_FLAG_TYPE, wmi.wbem_query_flag_type
req.header: wbemcli.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WBEM_QUERY_FLAG_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_WBEM_QUERY_FLAG_TYPE
 - wbemcli/tag_WBEM_QUERY_FLAG_TYPE
 - WBEM_QUERY_FLAG_TYPE
 - wbemcli/WBEM_QUERY_FLAG_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - WBEM_QUERY_FLAG_TYPE
---

# WBEM_QUERY_FLAG_TYPE enumeration


## -description

Contains flags used to define a query or  enumerator.

## -enum-fields

### -field WBEM_FLAG_DEEP:0

Include the specified class and all subclasses.

### -field WBEM_FLAG_SHALLOW:1

Include only the specified class, not any subclasses.

### -field WBEM_FLAG_PROTOTYPE:2

Used for prototyping. It does not execute the query and instead returns an object that looks like a typical result object.

## -see-also

<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenum">IWbemServices::CreateClassEnum</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync">IWbemServices::CreateClassEnumAsync</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum">IWbemServices::CreateInstanceEnum</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync">IWbemServices::CreateInstanceEnumAsync</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery">IWbemServices::ExecQuery</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync">IWbemServices::ExecQueryAsync</a>
