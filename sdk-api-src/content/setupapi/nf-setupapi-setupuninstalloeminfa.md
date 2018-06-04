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

# SetupUninstallOEMInfA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupUninstallOEMInf</b> function uninstalls a specified .inf file and any associated .pnf file. If the .inf file was installed with a catalog for signing drivers, the catalog is also removed. A caller of this function must have administrative privileges, otherwise the function fails.


## -parameters




### -param InfFileName [in]

File name, without path, of the .inf file in the Windows Inf directory that is to be uninstalled.


### -param Flags [in]

This parameter can be set as follows.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SUOI_FORCEDELETE"></a><a id="suoi_forcedelete"></a><dl>
<dt><b>SUOI_FORCEDELETE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The <b>SetupUninstallOEMInf</b> function first checks whether there are any devices installed using the .inf file. A device does not need to be  present to be detected as using the .inf file.

If this flag is not set and the function finds a currently installed device that was installed using this .inf file, the .inf file is not removed.

If this flag is set, the .inf file is removed whether  the function finds a device that was installed with this .inf file.

<div class="alert"><b>Note</b>  This flag only applies to x86, amd64, and ia64 architectures.  It is ignored on all other architectures.</div>
<div> </div>
<div class="alert"><b>Note</b>  If the driver package has any files that are copied to a <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/install/inf-destinationdirs-section">DestinationDir</a> that uses a <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/install/using-dirids">dirid</a> of 13, then this force flag is ignored.</div>
<div> </div>
</td>
</tr>
</table>
 


### -param Reserved [in]

Set to <b>null</b>.


## -returns



This function returns WINSETUPAPI BOOL.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/f082145d-b3e7-4efd-8820-3376a36f3710">SetupCopyOEMInf</a>
 

 

