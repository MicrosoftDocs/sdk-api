---
UID: NN:shobjidl_core.ICreatingProcess
title: ICreatingProcess
author: windows-sdk-content
description: Used by ShellExecuteEx and IContextMenu to allow the caller to alter some parameters of the process being created.
old-location: shell\icreatingprocess.htm
tech.root: shell
ms.assetid: 68B89E8C-2868-4F33-87A5-66A2FEFC0441
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ICreatingProcess, ICreatingProcess interface [Windows Shell], ICreatingProcess interface [Windows Shell],described, shell.icreatingprocess, shobjidl_core/ICreatingProcess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - ICreatingProcess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreatingProcess interface


## -description


Used by <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> and <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> to allow the caller to alter some parameters of the  process being created.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreatingProcess</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICreatingProcess</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreatingProcess</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5A13ABDB-8453-41BE-AF0C-B5A07486CBE6">OnCreating</a>
</td>
<td align="left" width="63%">
Allows you to modify the parameters of  the process being created.

</td>
</tr>
</table> 


## -remarks



 The caller should install an object into the site chain which implements <a href="https://msdn.microsoft.com/42026089-3e71-4483-ab35-1a6f305547fe">IServiceProvider::QueryService</a> and responds to the <b>SID_ExecuteCreatingProcess</b> service ID with an object that implements the <b>ICreatingProcess</b> interface.

After performing the desired operations, the object should forward the <a href="https://msdn.microsoft.com/5A13ABDB-8453-41BE-AF0C-B5A07486CBE6">ICreatingProcess::OnCreating</a> call up the site chain to allow other members of the site chain to participate.




## -see-also




<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/2C1756A3-FF40-4FBF-860D-06BB415DB695">ICreateProcessInputs</a>
 

 

