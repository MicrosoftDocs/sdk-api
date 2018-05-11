---
UID: NF:structuredquery.IQueryParser.SetOption
title: IQueryParser::SetOption
author: windows-driver-content
description: Sets a single option, such as a specified wordbreaker, for parsing an input string.
old-location: search\_search_IQueryParser_SetOption.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparser\setoption.htm
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IQueryParser interface [search],SetOption method, IQueryParser.SetOption, IQueryParser::SetOption, SetOption, SetOption method [search], SetOption method [search],IQueryParser interface, _search_IQueryParser_SetOption, search._search_IQueryParser_SetOption, structuredquery/IQueryParser::SetOption
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Structuredquery.h
api_name:
-	IQueryParser.SetOption
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IQueryParser::SetOption


## -description



          Sets a single option, such as a specified wordbreaker, for parsing an input string.


## -parameters




### -param option [in]

Type: <b><a href="https://msdn.microsoft.com/2753f0ad-2648-4ec2-b53f-089caad8ec15">STRUCTURED_QUERY_SINGLE_OPTION</a></b>


          Identifies the type of option to be set.
        


### -param pOptionValue [in]

Type: <b><a href="_stg_propvariant">PROPVARIANT</a>*</b>


          Pointer to a <a href="_stg_propvariant">PROPVARIANT</a> specifying the value to set for the <i>option</i> parameter. This value is interpreted differently depending on the value of the <i>option</i> parameter. 
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For more information, see <a href="https://msdn.microsoft.com/2753f0ad-2648-4ec2-b53f-089caad8ec15">STRUCTURED_QUERY_SINGLE_OPTION</a>.



