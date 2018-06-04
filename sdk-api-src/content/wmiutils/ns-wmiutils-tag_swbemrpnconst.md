---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tag_SWbemRpnConst structure


## -description


The <b>SWbemRpnConst</b> union defines the structure of the union used by WQL to process query tokens.


## -struct-fields




### -field m_pszStrVal

Pointer to a Unicode string value.


### -field m_bBoolVal

Boolean value.


### -field m_lLongVal

Signed long integer value.


### -field m_uLongVal

Unsigned long integer value.


### -field m_dblVal

Double precision floating-point value.


### -field m_lVal64

Signed 64-bit integer value.


### -field m_uVal64

Unsigned 64-bit integer value.


## -see-also




<a href="https://msdn.microsoft.com/4a0c0c1d-3d84-491f-8379-d164821fa71b">IWbemQuery</a>



<a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">IWbemQuery::GetAnalysis</a>



<a href="https://msdn.microsoft.com/04ef89e5-ce42-4d2d-8188-c2bbfe821bcc">SWbemRpnQueryToken</a>



<a href="https://msdn.microsoft.com/0f7e77a8-4ee6-421b-be4a-b58055a58c39">SWbemrpnEncodedQuery</a>
 

 

