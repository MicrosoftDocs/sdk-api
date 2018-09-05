---
UID: NF:shappmgr.IEnumPublishedApps.Reset
title: IEnumPublishedApps::Reset
author: windows-sdk-content
description: Resets the enumeration of IPublishedApp objects to the first item.
old-location: shell\IEnumPublishedApps_Reset.htm
old-project: shell
ms.assetid: 007f6636-725a-4af5-ad3f-578f8183a088
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IEnumPublishedApps interface [Windows Shell],Reset method, IEnumPublishedApps.Reset, IEnumPublishedApps::Reset, Reset, Reset method [Windows Shell], Reset method [Windows Shell],IEnumPublishedApps interface, inet_IEnumPublishedApps_Reset, shappmgr/IEnumPublishedApps::Reset, shell.IEnumPublishedApps_Reset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shappmgr.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PUBAPPINFOFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shappmgr.h
api_name:
 - IEnumPublishedApps.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IEnumPublishedApps::Reset


## -description


Resets the enumeration of <a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a> objects to the first item.
		


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns the following value.

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
This method only returns S_OK.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/89a06b1d-1b72-46ca-91cd-bb63ea0cbff7">IEnumPublishedApps</a> is not a standard enumeration interface.</div>
<div> </div>
 It does not support a Skip method nor does its Next method support retrieval of multiple items.




## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>



<a href="https://msdn.microsoft.com/89a06b1d-1b72-46ca-91cd-bb63ea0cbff7">IEnumPublishedApps</a>



<a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a>
 

 

