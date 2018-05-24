---
UID: NE:structuredquery.tagSTRUCTURED_QUERY_SYNTAX
title: tagSTRUCTURED_QUERY_SYNTAX
author: windows-driver-content
description: Specifies the type of query syntax.
old-location: search\_search_STRUCTURED_QUERY_SYNTAX.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\structured_query_syntax.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: SQS_ADVANCED_QUERY_SYNTAX, SQS_NATURAL_QUERY_SYNTAX, SQS_NO_SYNTAX, STRUCTURED_QUERY_SYNTAX, STRUCTURED_QUERY_SYNTAX enumeration [search], _search_STRUCTURED_QUERY_SYNTAX, search._search_STRUCTURED_QUERY_SYNTAX, structuredquery/SQS_ADVANCED_QUERY_SYNTAX, structuredquery/SQS_NATURAL_QUERY_SYNTAX, structuredquery/SQS_NO_SYNTAX, structuredquery/STRUCTURED_QUERY_SYNTAX, tagSTRUCTURED_QUERY_SYNTAX
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UnalignedStringCchLengthW (Unicode) and StringCchLengthA (ANSI)
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STRUCTURED_QUERY_SYNTAX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Structuredquery.h
api_name:
-	STRUCTURED_QUERY_SYNTAX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# tagSTRUCTURED_QUERY_SYNTAX enumeration


## -description


Specifies the type of query syntax. 


## -enum-fields




### -field SQS_NO_SYNTAX


        No syntax.
      


### -field SQS_ADVANCED_QUERY_SYNTAX


      Specifies the Advanced Query Syntax. For example, "kind:email to:david to:bill".
      


### -field SQS_NATURAL_QUERY_SYNTAX


      Specifies the Natural Query Syntax. This syntax removes the requirement for a colon between properties and values, for example, "email from david to bill".
      


## -remarks



Use this enumeration to set the desired SQSO_SYNTAX flag in <a href="https://msdn.microsoft.com/2753f0ad-2648-4ec2-b53f-089caad8ec15">STRUCTURED_QUERY_SINGLE_OPTION</a>, which is used with the methods <a href="https://msdn.microsoft.com/a7c2d4d7-7ccf-4daa-b4d5-cf23ed1e88b4">IQueryParser::SetOption</a> and <a href="https://msdn.microsoft.com/85216ad7-6988-43cd-87b3-49a2ca1173b6">IQueryParser::GetOption</a>.



