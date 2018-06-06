---
UID: NS:wmiutils.tag_SWbemRpnConst
title: tag_SWbemRpnConst
author: windows-sdk-content
description: Defines the structure of the union used by WQL to process query tokens.
old-location: wmi\swbemrpnconst.htm
old-project: WmiSdk
ms.assetid: 06b2feff-b604-44d2-8381-719575650e88
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: SWbemRpnConst, SWbemRpnConst union [Windows Management Instrumentation], tag_SWbemRpnConst, wmi.swbemrpnconst, wmiutils/SWbemRpnConst
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SWbemRpnConst
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmiutils.h
api_name:
 - SWbemRpnConst
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

