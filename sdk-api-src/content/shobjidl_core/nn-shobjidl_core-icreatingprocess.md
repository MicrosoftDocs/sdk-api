---
UID: NN:shobjidl_core.ICreatingProcess
title: ICreatingProcess (shobjidl_core.h)
description: Used by ShellExecuteEx and IContextMenu to allow the caller to alter some parameters of the process being created.
helpviewer_keywords: ["ICreatingProcess","ICreatingProcess interface [Windows Shell]","ICreatingProcess interface [Windows Shell]","described","shell.icreatingprocess","shobjidl_core/ICreatingProcess"]
old-location: shell\icreatingprocess.htm
tech.root: shell
ms.assetid: 68B89E8C-2868-4F33-87A5-66A2FEFC0441
ms.date: 08/02/2022
ms.keywords: ICreatingProcess, ICreatingProcess interface [Windows Shell], ICreatingProcess interface [Windows Shell],described, shell.icreatingprocess, shobjidl_core/ICreatingProcess
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICreatingProcess
 - shobjidl_core/ICreatingProcess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ICreatingProcess
---

# ICreatingProcess interface


## -description

Used by <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> to allow the caller to alter some parameters of the  process being created.

## -inheritance

The <b>ICreatingProcess</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICreatingProcess</b> also has these types of members:

## -remarks

 The caller should install an object into the site chain which implements <a href="/dotnet/api/microsoft.visualstudio.shell.package.microsoft-visualstudio-ole-interop-iserviceprovider-queryservice?view=visualstudiosdk-2017&preserve-view=true">IServiceProvider::QueryService</a> and responds to the <b>SID_ExecuteCreatingProcess</b> service ID with an object that implements the <b>ICreatingProcess</b> interface.

After performing the desired operations, the object should forward the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreatingprocess-oncreating">ICreatingProcess::OnCreating</a> call up the site chain to allow other members of the site chain to participate.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs">ICreateProcessInputs</a>
