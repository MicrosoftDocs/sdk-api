---
UID: NF:ncryptprotect.NCryptStreamClose
title: NCryptStreamClose function (ncryptprotect.h)
author: windows-sdk-content
description: Closes a data protection stream object opened by using the NCryptStreamOpenToProtect or NCryptStreamOpenToUnprotect functions.
old-location: security\ncryptstreamclose.htm
tech.root: SecCNG
ms.assetid: 770640F2-04C7-4512-8004-41F4ECDC110E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NCryptStreamClose, NCryptStreamClose function [Security], ncryptprotect/NCryptStreamClose, security.ncryptstreamclose
ms.topic: function
req.header: ncryptprotect.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NCrypt.lib
req.dll: NCrypt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NCrypt.dll
api_name:
 - NCryptStreamClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NCryptStreamClose function


## -description


The <b>NCryptStreamClose</b> function closes a data protection stream object opened by using the <a href="https://msdn.microsoft.com/7DE74BB1-1B84-4721-BE4A-4D2661E93E00">NCryptStreamOpenToProtect</a> or <a href="https://msdn.microsoft.com/9848082E-EDDA-4DA1-9896-42EAF2ADFAB4">NCryptStreamOpenToUnprotect</a> functions.


## -parameters




### -param hStream [in]

Data stream handle returned by <a href="https://msdn.microsoft.com/7DE74BB1-1B84-4721-BE4A-4D2661E93E00">NCryptStreamOpenToProtect</a> or <a href="https://msdn.microsoft.com/9848082E-EDDA-4DA1-9896-42EAF2ADFAB4">NCryptStreamOpenToUnprotect</a>.


## -returns



Returns a status code that indicates the success or failure of the function. Possible return codes include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified by the <i>hStream</i> parameter is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/591C7361-334E-4A65-8616-C0ED3BBC2297">CNG DPAPI Functions</a>



<a href="https://msdn.microsoft.com/7DE74BB1-1B84-4721-BE4A-4D2661E93E00">NCryptStreamOpenToProtect</a>



<a href="https://msdn.microsoft.com/9848082E-EDDA-4DA1-9896-42EAF2ADFAB4">NCryptStreamOpenToUnprotect</a>



<a href="https://msdn.microsoft.com/417F9267-6055-489C-AF26-BEF5E17CB8B4">NCryptStreamUpdate</a>
 

 

