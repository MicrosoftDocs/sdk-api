---
UID: NE:msclus.CLUSTER_PROPERTY_FORMAT
title: CLUSTER_PROPERTY_FORMAT (msclus.h)
description: Specifies the data type of a property value in a property list.
helpviewer_keywords: ["CLUSPROP_FORMAT_BINARY","CLUSPROP_FORMAT_DWORD","CLUSPROP_FORMAT_EXPANDED_SZ","CLUSPROP_FORMAT_EXPAND_SZ","CLUSPROP_FORMAT_FILETIME","CLUSPROP_FORMAT_LARGE_INTEGER","CLUSPROP_FORMAT_LONG","CLUSPROP_FORMAT_MULTI_SZ","CLUSPROP_FORMAT_SECURITY_DESCRIPTOR","CLUSPROP_FORMAT_SZ","CLUSPROP_FORMAT_ULARGE_INTEGER","CLUSPROP_FORMAT_UNKNOWN","CLUSPROP_FORMAT_USER","CLUSPROP_FORMAT_WORD","CLUSTER_PROPERTY_FORMAT","CLUSTER_PROPERTY_FORMAT enumeration [Failover Cluster]","_CLUSTER_PROPERTY_FORMAT","_CLUSTER_PROPERTY_FORMAT enumeration [Failover Cluster]","clusapi/CLUSPROP_FORMAT_BINARY","clusapi/CLUSPROP_FORMAT_DWORD","clusapi/CLUSPROP_FORMAT_EXPANDED_SZ","clusapi/CLUSPROP_FORMAT_EXPAND_SZ","clusapi/CLUSPROP_FORMAT_FILETIME","clusapi/CLUSPROP_FORMAT_LARGE_INTEGER","clusapi/CLUSPROP_FORMAT_LONG","clusapi/CLUSPROP_FORMAT_MULTI_SZ","clusapi/CLUSPROP_FORMAT_SECURITY_DESCRIPTOR","clusapi/CLUSPROP_FORMAT_SZ","clusapi/CLUSPROP_FORMAT_ULARGE_INTEGER","clusapi/CLUSPROP_FORMAT_UNKNOWN","clusapi/CLUSPROP_FORMAT_USER","clusapi/CLUSPROP_FORMAT_WORD","clusapi/CLUSTER_PROPERTY_FORMAT","clusapi/_CLUSTER_PROPERTY_FORMAT","msclus/CLUSPROP_FORMAT_BINARY","msclus/CLUSPROP_FORMAT_DWORD","msclus/CLUSPROP_FORMAT_EXPANDED_SZ","msclus/CLUSPROP_FORMAT_EXPAND_SZ","msclus/CLUSPROP_FORMAT_FILETIME","msclus/CLUSPROP_FORMAT_LARGE_INTEGER","msclus/CLUSPROP_FORMAT_LONG","msclus/CLUSPROP_FORMAT_MULTI_SZ","msclus/CLUSPROP_FORMAT_SECURITY_DESCRIPTOR","msclus/CLUSPROP_FORMAT_SZ","msclus/CLUSPROP_FORMAT_ULARGE_INTEGER","msclus/CLUSPROP_FORMAT_UNKNOWN","msclus/CLUSPROP_FORMAT_USER","msclus/CLUSPROP_FORMAT_WORD","msclus/CLUSTER_PROPERTY_FORMAT","msclus/_CLUSTER_PROPERTY_FORMAT","mscs.cluster_property_format"]
old-location: mscs\cluster_property_format.htm
tech.root: MsCS
ms.assetid: a5e06aaf-96ef-41e9-ab73-c0edc8f34d12
ms.date: 12/05/2018
ms.keywords: CLUSPROP_FORMAT_BINARY, CLUSPROP_FORMAT_DWORD, CLUSPROP_FORMAT_EXPANDED_SZ, CLUSPROP_FORMAT_EXPAND_SZ, CLUSPROP_FORMAT_FILETIME, CLUSPROP_FORMAT_LARGE_INTEGER, CLUSPROP_FORMAT_LONG, CLUSPROP_FORMAT_MULTI_SZ, CLUSPROP_FORMAT_SECURITY_DESCRIPTOR, CLUSPROP_FORMAT_SZ, CLUSPROP_FORMAT_ULARGE_INTEGER, CLUSPROP_FORMAT_UNKNOWN, CLUSPROP_FORMAT_USER, CLUSPROP_FORMAT_WORD, CLUSTER_PROPERTY_FORMAT, CLUSTER_PROPERTY_FORMAT enumeration [Failover Cluster], _CLUSTER_PROPERTY_FORMAT, _CLUSTER_PROPERTY_FORMAT enumeration [Failover Cluster], clusapi/CLUSPROP_FORMAT_BINARY, clusapi/CLUSPROP_FORMAT_DWORD, clusapi/CLUSPROP_FORMAT_EXPANDED_SZ, clusapi/CLUSPROP_FORMAT_EXPAND_SZ, clusapi/CLUSPROP_FORMAT_FILETIME, clusapi/CLUSPROP_FORMAT_LARGE_INTEGER, clusapi/CLUSPROP_FORMAT_LONG, clusapi/CLUSPROP_FORMAT_MULTI_SZ, clusapi/CLUSPROP_FORMAT_SECURITY_DESCRIPTOR, clusapi/CLUSPROP_FORMAT_SZ, clusapi/CLUSPROP_FORMAT_ULARGE_INTEGER, clusapi/CLUSPROP_FORMAT_UNKNOWN, clusapi/CLUSPROP_FORMAT_USER, clusapi/CLUSPROP_FORMAT_WORD, clusapi/CLUSTER_PROPERTY_FORMAT, clusapi/_CLUSTER_PROPERTY_FORMAT, msclus/CLUSPROP_FORMAT_BINARY, msclus/CLUSPROP_FORMAT_DWORD, msclus/CLUSPROP_FORMAT_EXPANDED_SZ, msclus/CLUSPROP_FORMAT_EXPAND_SZ, msclus/CLUSPROP_FORMAT_FILETIME, msclus/CLUSPROP_FORMAT_LARGE_INTEGER, msclus/CLUSPROP_FORMAT_LONG, msclus/CLUSPROP_FORMAT_MULTI_SZ, msclus/CLUSPROP_FORMAT_SECURITY_DESCRIPTOR, msclus/CLUSPROP_FORMAT_SZ, msclus/CLUSPROP_FORMAT_ULARGE_INTEGER, msclus/CLUSPROP_FORMAT_UNKNOWN, msclus/CLUSPROP_FORMAT_USER, msclus/CLUSPROP_FORMAT_WORD, msclus/CLUSTER_PROPERTY_FORMAT, msclus/_CLUSTER_PROPERTY_FORMAT, mscs.cluster_property_format
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
req.typenames: CLUSTER_PROPERTY_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_PROPERTY_FORMAT
 - msclus/CLUSTER_PROPERTY_FORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_PROPERTY_FORMAT
---

# CLUSTER_PROPERTY_FORMAT enumeration


## -description

Specifies the data type of a property value in a 
    <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a>.

## -enum-fields

### -field CLUSPROP_FORMAT_UNKNOWN:0

Data is in an unknown format.

### -field CLUSPROP_FORMAT_BINARY

Data is a binary value.

### -field CLUSPROP_FORMAT_DWORD

Data is a <b>DWORD</b> value.

### -field CLUSPROP_FORMAT_SZ

Data is a null-terminated Unicode string.

### -field CLUSPROP_FORMAT_EXPAND_SZ

Data is a null-terminated Unicode string with unexpanded references to environment variables.

### -field CLUSPROP_FORMAT_MULTI_SZ

Data is an array of null-terminated Unicode strings.

### -field CLUSPROP_FORMAT_ULARGE_INTEGER

Data is an <b>ULARGE_INTEGER</b>.

### -field CLUSPROP_FORMAT_LONG

Data is a signed <b>LONG</b> value.

### -field CLUSPROP_FORMAT_EXPANDED_SZ

Data is a null-terminated Unicode string with expanded references to environment variables.

### -field CLUSPROP_FORMAT_SECURITY_DESCRIPTOR

Data is a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> in 
          <a href="/windows/desktop/SecGloss/s-gly">self-relative</a> 
          format. For more information about self-relative security descriptors, see 
          <a href="/windows/desktop/SecAuthZ/absolute-and-self-relative-security-descriptors">Absolute and Self-Relative Security Descriptors</a>.

### -field CLUSPROP_FORMAT_LARGE_INTEGER

Data is a signed <b>LARGE_INTEGER</b>.

### -field CLUSPROP_FORMAT_WORD

Data is a <b>WORD</b> value.

### -field CLUSPROP_FORMAT_FILETIME

Data is a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.

### -field CLUSPROP_FORMAT_VALUE_LIST

### -field CLUSPROP_FORMAT_PROPERTY_LIST

### -field CLUSPROP_FORMAT_USER:32768

Reserved for future use.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/previous-versions/windows/desktop/mscs/clusproperty-format">Format Property of the ClusProperty Object</a>



<a href="/previous-versions/windows/desktop/mscs/cluspropertyvalue-format">Format Property of the ClusPropertyValue Object</a>
