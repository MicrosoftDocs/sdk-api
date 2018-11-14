---
UID: NS:wmiutils.tag_SWbemQueryQualifiedName
title: tag_SWbemQueryQualifiedName
author: windows-sdk-content
description: The SWbemQueryQualifiedName structure stores property names for the IWbemQuery::GetAnalysis method.
old-location: wmi\swbemqueryqualifiedname.htm
tech.root: WmiSdk
ms.assetid: ce8031a1-b30f-4ff6-90d8-42e46e1b6d89
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: SWbemQueryQualifiedName, SWbemQueryQualifiedName structure [Windows Management Instrumentation], tag_SWbemQueryQualifiedName, wmi.swbemqueryqualifiedname, wmiutils/SWbemQueryQualifiedName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wmiutils.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmiutils.h
api_name:
 - SWbemQueryQualifiedName
product: Windows
targetos: Windows
req.typenames: SWbemQueryQualifiedName
req.redist: 
---

# tag_SWbemQueryQualifiedName structure


## -description


The <b>SWbemQueryQualifiedName</b> structure stores property names for the <a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">IWbemQuery::GetAnalysis</a> method.


## -struct-fields




### -field m_uVersion

Unused. Always 1 (one).


### -field m_uTokenType

Unused. Always 1 (one).


### -field m_uNameListSize

Number of elements in the list of names. For example, for the  "propName" property,  <b>m_uNameListSize</b> is 1 (one) and <b>m_ppszNameList</b> is "propName".


### -field m_ppszNameList

List of property names. For example, for the  "propName" property, <b>m_uNameListSize</b> is 1 (one) and <b>m_ppszNameList</b> is "propName".


### -field m_bArraysUsed

Unused. Always <b>false</b>.


### -field m_pbArrayElUsed

Unused. Always <b>NULL</b>.


### -field m_puArrayIndex

Unused. Always <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/4a0c0c1d-3d84-491f-8379-d164821fa71b">IWbemQuery</a>



<a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">IWbemQuery::GetAnalysis</a>



<a href="https://msdn.microsoft.com/0f7e77a8-4ee6-421b-be4a-b58055a58c39">SWbemRpnEncodedQuery</a>
 

 

