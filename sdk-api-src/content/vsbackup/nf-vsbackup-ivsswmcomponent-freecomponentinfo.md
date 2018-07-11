---
UID: NF:vsbackup.IVssWMComponent.FreeComponentInfo
title: IVssWMComponent::FreeComponentInfo
author: windows-sdk-content
description: The FreeComponentInfo method deallocates system resources devoted to the specified component information.
old-location: base\ivsswmcomponent_freecomponentinfo.htm
old-project: vss
ms.assetid: 3f0c4634-2b1c-4a9b-9c13-ace38e03a7ce
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: FreeComponentInfo, FreeComponentInfo method [VSS], FreeComponentInfo method [VSS],IVssWMComponent interface, IVssWMComponent interface [VSS],FreeComponentInfo method, IVssWMComponent.FreeComponentInfo, IVssWMComponent::FreeComponentInfo, _win32_ivsswmcomponent_freecomponentinfo, base.ivsswmcomponent_freecomponentinfo, vsbackup/IVssWMComponent::FreeComponentInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssWMComponent.FreeComponentInfo
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssWMComponent::FreeComponentInfo


## -description


The 
<b>FreeComponentInfo</b> method deallocates system resources devoted to the specified component information.


## -parameters




### -param pInfo [out]

Pointer to a 
<a href="https://msdn.microsoft.com/9723e90e-cd5e-4815-843b-8ed8632ebe45">VSS_COMPONENTINFO</a> structure that contains the component information.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully freed the component information data.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8567ca7f-dc50-4cf2-b3c1-a2ae8d55dc95">IVssWMComponent</a>



<a href="https://msdn.microsoft.com/9723e90e-cd5e-4815-843b-8ed8632ebe45">VSS_COMPONENTINFO</a>
 

 

