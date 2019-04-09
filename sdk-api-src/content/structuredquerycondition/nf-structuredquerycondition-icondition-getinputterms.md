---
UID: NF:structuredquerycondition.ICondition.GetInputTerms
title: ICondition::GetInputTerms (structuredquerycondition.h)
author: windows-sdk-content
description: For a leaf node, ICondition::GetInputTerms retrieves information about what parts (or ranges) of the input string produced the property, the operation, and the value for the search condition node.
old-location: search\_search_ICondition_GetInputTerms.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\getinputterms.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetInputTerms, GetInputTerms method [search], GetInputTerms method [search],ICondition interface, ICondition interface [search],GetInputTerms method, ICondition.GetInputTerms, ICondition::GetInputTerms, _search_ICondition_GetInputTerms, search._search_ICondition_GetInputTerms, structuredquerycondition/ICondition::GetInputTerms
ms.topic: method
req.header: structuredquerycondition.h
req.include-header: Structuredquery.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - structuredquerycondition.h
api_name:
 - ICondition.GetInputTerms
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ICondition::GetInputTerms


## -description


For a leaf node, <b>ICondition::GetInputTerms</b> retrieves information about what parts (or ranges) of the input string produced the property, the operation, and the value for the search condition node.


## -parameters




### -param ppPropertyTerm [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb231336(v=VS.85).aspx">IRichChunk</a>**</b>

Receives a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb231336(v=VS.85).aspx">IRichChunk</a> interface that provides information about what part of the input string produced the property of the leaf node, if that can be determined; otherwise, this parameter is set to <b>NULL</b>.


### -param ppOperationTerm [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb231336(v=VS.85).aspx">IRichChunk</a>**</b>

Receives a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb231336(v=VS.85).aspx">IRichChunk</a> interface that provides information about what part of the input string produced the operation of the leaf node, if that can be determined; otherwise, this parameter is set to <b>NULL</b>.


### -param ppValueTerm [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb231336(v=VS.85).aspx">IRichChunk</a>**</b>

Receives a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb231336(v=VS.85).aspx">IRichChunk</a> interface that provides information about what part of the input string produced the value of the leaf node, if that can be determined; otherwise, this parameter is set to <b>NULL</b>.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Any or all of the parameters <i>ppPropertyTerm</i>, <i>ppOperationTerm</i> and <i>ppValueTerm</i> can be <b>NULL</b>.

Each <a href="https://msdn.microsoft.com/en-us/library/Bb231336(v=VS.85).aspx">IRichChunk</a> object retrieved by this method represents a range of tokens from the input string. The range tokens identifies the substring that produced the property, operation, or value of the input string. The <b>IRichChunk</b>'s <a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a> out parameter is not used.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965692(v=VS.85).aspx">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>



<b>Reference</b>
 

 

