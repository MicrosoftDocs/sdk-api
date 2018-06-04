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

# __MIDL___MIDL_itf_gpmgmt_0000_0000_0008 enumeration


## -description


<b>GPMReportingOptions</b> defines options for Group Policy Management Console  reports.

<b>GPMReportingOptions</b> defines options for Group Policy Management Console reports.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef enum {
        opReportLegacy = 0,
        opReportComments = 1,
        } GPMReportingOptions;</pre>
</td>
</tr>
</table></span></div>

## -enum-fields




### -field opReportLegacy

Use administrative template ADM files.


### -field opReportComments

Include comments.

