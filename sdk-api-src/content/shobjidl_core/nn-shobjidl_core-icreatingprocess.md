---
UID: NN:shobjidl_core.ICreatingProcess
title: ICreatingProcess (shobjidl_core.h)
description: Used by ShellExecuteEx and IContextMenu to allow the caller to alter some parameters of the process being created.
old-location: shell\icreatingprocess.htm
tech.root: shell
ms.assetid: 68B89E8C-2868-4F33-87A5-66A2FEFC0441
ms.date: 12/05/2018
ms.keywords: ICreatingProcess, ICreatingProcess interface [Windows Shell], ICreatingProcess interface [Windows Shell],described, shell.icreatingprocess, shobjidl_core/ICreatingProcess
f1_keywords:
- shobjidl_core/ICreatingProcess
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICreatingProcess interface


## -description


Used by <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> and <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> to allow the caller to alter some parameters of the  process being created.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreatingProcess</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICreatingProcess</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreatingprocess-oncreating">OnCreating</a>
</td>
<td align="left" width="63%">
Allows you to modify the parameters of  the process being created.

</td>
</tr>
</table> 


## -remarks



 The caller should install an object into the site chain which implements <a href="https://docs.microsoft.com/dotnet/api/microsoft.visualstudio.shell.package.microsoft-visualstudio-ole-interop-iserviceprovider-queryservice?view=visualstudiosdk-2017">IServiceProvider::QueryService</a> and responds to the <b>SID_ExecuteCreatingProcess</b> service ID with an object that implements the <b>ICreatingProcess</b> interface.

After performing the desired operations, the object should forward the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreatingprocess-oncreating">ICreatingProcess::OnCreating</a> call up the site chain to allow other members of the site chain to participate.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs">ICreateProcessInputs</a>
 

 

