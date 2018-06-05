---
UID: NF:traffic.TcCloseInterface
title: TcCloseInterface function
author: windows-sdk-content
description: The TcCloseInterface function closes an interface previously opened with a call to TcOpenInterface. All flows and filters on a particular interface should be closed before closing the interface with a call to TcCloseInterface.
old-location: qos\tccloseinterface.htm
old-project: QOS
ms.assetid: c7c78f98-0890-4889-994e-bbac08ba9c44
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: TcCloseInterface, TcCloseInterface function [QOS], _gqos_tccloseinterface, qos.tccloseinterface, traffic/TcCloseInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: traffic.h
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
tech.root: 
req.typenames: TPMVSCMGR_ERROR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Traffic.dll
api_name:
-	TcCloseInterface
product: Windows
targetos: Windows
req.lib: Traffic.lib
req.dll: Traffic.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TcCloseInterface function


## -description


The 
<b>TcCloseInterface</b> function closes an interface previously opened with a call to 
<a href="https://msdn.microsoft.com/8c7e658c-862f-4715-9ba5-ac079db924a1">TcOpenInterface</a>. All flows and filters on a particular interface should be closed before closing the interface with a call to 
<b>TcCloseInterface</b>.


## -parameters




### -param IfcHandle [in]

Handle associated with the interface to be closed. This handle is obtained by a previous call to the 
<a href="https://msdn.microsoft.com/8c7e658c-862f-4715-9ba5-ac079db924a1">TcOpenInterface</a> function.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The function executed without errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The interface handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TC_SUPPORTED_OBJECTS_EXIST</b></dt>
</dl>
</td>
<td width="60%">
Not all flows have been deleted for this interface.

</td>
</tr>
</table>
 




## -remarks



Regardless of whether 
<b>TcCloseInterface</b> is called, an interface will be closed following a TC_NOTIFY_IFC_CLOSE notification event. If the 
<b>TcCloseInterface</b> function is called with the handle of an interface that has already been closed, the handle will be invalidated and 
<b>TcCloseInterface</b> will return ERROR_INVALID_HANDLE.

<div class="alert"><b>Note</b>  Use of 
<b>TcCloseInterface</b> requires administrative privilege.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/8c7e658c-862f-4715-9ba5-ac079db924a1">TcOpenInterface</a>
 

 

