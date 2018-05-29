---
UID: NF:propsys.PSRefreshPropertySchema
title: PSRefreshPropertySchema function
author: windows-sdk-content
description: Not supported.It is valid to call this function, but it is not implemented to perform any function so there is no reason to do so.
old-location: properties\PSRefreshPropertySchema.htm
old-project: properties
ms.assetid: 07efbf66-3594-4b9d-b959-278dc9000572
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: PSRefreshPropertySchema, PSRefreshPropertySchema function [Windows Properties], properties.PSRefreshPropertySchema, propsys/PSRefreshPropertySchema, shell.PSRefreshPropertySchema, shell_PSRefreshPropertySchema
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propsys.h
req.include-header: Propsys.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PSRefreshPropertySchema
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 5.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PSRefreshPropertySchema function


## -description


Not supported.

It is valid to call this function, but it is not implemented to perform any function so there is no reason to do so.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Schema files reloaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling context does not have proper privileges.

</td>
</tr>
</table>
 



