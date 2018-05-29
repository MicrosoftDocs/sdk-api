---
UID: NE:structuredquery.CASE_REQUIREMENT
title: CASE_REQUIREMENT
author: windows-sdk-content
description: Specifies the case requirements of keywords, if any, for a query.
old-location: search\_search_CASE_REQUIREMENT.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\case_requirement.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: CASE_REQUIREMENT, CASE_REQUIREMENT enumeration [search], CASE_REQUIREMENT_ANY, CASE_REQUIREMENT_UPPER_IF_AQS, _search_CASE_REQUIREMENT, search._search_CASE_REQUIREMENT, structuredquery/CASE_REQUIREMENT, structuredquery/CASE_REQUIREMENT_ANY, structuredquery/CASE_REQUIREMENT_UPPER_IF_AQS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCchVPrintf_lW (Unicode) and StringCchVPrintf_lA (ANSI)
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CASE_REQUIREMENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Structuredquery.h
api_name:
-	CASE_REQUIREMENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# CASE_REQUIREMENT enumeration


## -description


Specifies the case requirements of keywords, if any, for a query. 


## -enum-fields




### -field CASE_REQUIREMENT_ANY


        Keywords are recognized regardless of case.
      


### -field CASE_REQUIREMENT_UPPER_IF_AQS


      	Keywords are recognized only if uppercase when AQS is the syntax. When AQS is not the syntax, keywords are recognized regardless of case.
      


## -remarks



Keywords include Boolean operators such as AND, NOT, and OR.




## -see-also




<a href="https://msdn.microsoft.com/84a052ae-4d05-438f-ab90-e1a248239aca">STRUCTURED_QUERY_RESOLVE_OPTION</a>
 

 

