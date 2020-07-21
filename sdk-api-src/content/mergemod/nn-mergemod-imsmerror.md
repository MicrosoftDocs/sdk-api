---
UID: NN:mergemod.IMsmError
title: IMsmError (mergemod.h)
description: The IMsmError interface retrieves details about a single merge error.
helpviewer_keywords: ["IMsmError","IMsmError interface","IMsmError interface","described","mergemod/IMsmError","setup.imsmerror_interface"]
old-location: setup\imsmerror_interface.htm
tech.root: Msi
ms.assetid: 705f53ca-82f4-4929-b2a3-0ace8e4ca19b
ms.date: 12/05/2018
ms.keywords: IMsmError, IMsmError interface, IMsmError interface,described, mergemod/IMsmError, setup.imsmerror_interface
f1_keywords:
- mergemod/IMsmError
dev_langs:
- c++
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mergemod.dll
api_name:
- IMsmError
- IMsmError.get_Type
- IMsmError.get_Path
- IMsmError.get_Language
- IMsmError.get_DatabaseTable
- IMsmError.get_DatabaseKeys
- IMsmError.get_ModuleTable
- IMsmError.get_ModuleKeys
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMsmError interface


## -description


The <b>IMsmError</b> interface retrieves details about a single merge error.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmError</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMsmError</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMsmError</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_DatabaseKeys</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/error-databasekeys">DatabaseKeys</a> property of the <a href="https://docs.microsoft.com/windows/desktop/Msi/error-object">Error</a> object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_DatabaseTable</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/error-databasetable">DatabaseTable</a> property of the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/error-object">Error</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_Language</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/dependency-language">Language</a> property of the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/error-object">Error</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_ModuleKeys</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/error-modulekeys">ModuleKeys</a> property of the <a href="https://docs.microsoft.com/windows/desktop/Msi/error-object">Error</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_ModuleTable</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/error-moduletable">ModuleTable</a> property of the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/error-object">Error</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_Path</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/error-path">Path</a> property of the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/error-object">Error</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_Type</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/error-type">Type</a> property of the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/error-object">Error</a> object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>
 

 

