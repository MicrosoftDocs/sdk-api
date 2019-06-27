---
UID: NS:cmdtree.tagDBPARAMETER
title: DBPARAMETER (cmdtree.h)
author: windows-sdk-content
description: The DBPARAMETER structure is used to define values for scalar parameters.
old-location: indexsrv\dbparameter.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_2p0y.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DBPARAMETER, DBPARAMETER structure [Indexing Service], _idxs_DBPARAMETER, cmdtree/DBPARAMETER, indexsrv.dbparameter, tagDBPARAMETER
ms.topic: struct
f1_keywords: 
 - "cmdtree/DBPARAMETER"
req.header: cmdtree.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - cmdtree.h
api_name:
 - DBPARAMETER
product: Windows
targetos: Windows
req.typenames: DBPARAMETER
req.redist: 
ms.custom: 19H1
---

# DBPARAMETER structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href="http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>DBPARAMETER</b> structure is used to define values for scalar parameters. 


## -struct-fields




### -field pwszName

parameter name


### -field pTypeInfo

if not a null pointer, type is described
                             by the ITypeInfo


### -field pNum

 Structure describing the
                             precision, scale and value of the numeric value.


### -field cbMaxLength

the maximum length of the parameter


### -field dwFlags

bitmask describing parameter characteristics


### -field wType

type of the parameter


## -remarks



Note that there is no entry for the ordinal position of the parameter. The assumption is that the ordinal position will be determined by the provider after evaluating the tree as a whole, and not by assigning a specific value to an individual member within the tree. Data consumers can determine the ordinal position based on the name using <b>ICommandWithParameters::MapParameterNames</b>. For more information about the interface, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ms712937(v=vs.85)">ICommandWithParameters</a>.



