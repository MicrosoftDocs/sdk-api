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

# SetupDiGetActualModelsSectionA function


## -description


The <b>SetupDiGetActualModelsSection</b> function retrieves the appropriate decorated <a href="devinst.inf_models_section">INF Models section</a> to use when installing a device from a device INF file.


## -parameters




### -param Context [in]

A pointer to an INF file context that specifies a <i>manufacturer-identifier</i> entry in an <a href="devinst.inf_manufacturer_section">INF Manufacturer section</a> of an INF file. The <i>manufacturer-identifier</i> entry specifies an INF <i>Models</i> section name and optionally specifies <i>TargetOSVersion</i> decorations for the <i>Models</i> section name. For information about INF files and an INF file context, see the Platform SDK topics on <a href="http://go.microsoft.com/fwlink/p/?linkid=81350">using INF files</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=81351">INFCONTEXT structure</a>. 


### -param AlternatePlatformInfo [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552338">SP_ALTPLATFORM_INFO</a> structure that supplies information about a Windows version and processor architecture. The <b>cbSize</b> member of this structure must be set to <b>sizeof(</b>SP_ALTPLATFORM_INFO_V2<b>)</b>. This parameter is optional and can be set to <b>NULL</b>.


### -param InfSectionWithExt

TBD


### -param InfSectionWithExtSize

TBD


### -param RequiredSize [out, optional]

A pointer to a DWORD-type variable that receives the size, in characters, of the <i>DecoratedModelsSection</i> buffer that is required to retrieve the decorated <i>Models</i> section name and a terminating NULL character. This parameter is optional and can be set to <b>NULL</b>.


### -param Reserved

Reserved for internal system use. This parameter must be set to <b>NULL</b>.


#### - DecoratedModelsSection [out, optional]

A pointer to a buffer that receives a string that contains the decorated INF <i>Models</i> section name and a NULL terminator. If <i>AlternatePlatformInfo</i> is not supplied, the decorated INF <i>Models</i> section name applies to the current platform; otherwise the name applies to the specified alternative platform. This parameter is optional and can be set to <b>NULL</b>. If this parameter is <b>NULL</b>, the function returns <b>TRUE</b> and sets <i>RequiredSize</i> to the size, in characters, that is required to return the decorated <i>Models</i> section name and a terminating NULL character. 


#### - DecoratedModelsSectionSize [in]

 The size, in characters, of the <i>DecoratedModelsSection </i>buffer. If <i>DecoratedModelsSection</i> is <b>NULL</b>, this parameter must be set to zero.


## -returns



<b>SetupDiGetActualModelsSection</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, the function returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



<b>SetupDiGetActualModelsSection</b> determines which <i>TargetOSVersion</i> fields in the <i>manufacturer-identifier</i> entry (supplied by <i>Context</i>) apply to the current platform, if <i>AlternatePlatformInfo</i> is not supplied, or to an alternative platform, if alternative platform information is supplied. <b>SetupDiGetActualModelsSection</b> selects the most appropriate platform based on all the <i>TargetOSVersion</i> fields, appends the <i>TargetOSVersion</i> string to the INF <i>Models</i> section name, and returns the decorated INF <i>Models</i> section name to the caller. In a <i>manufacturer-identifier</i> entry, the operating system major version is specified by the <i>OSMajorVersion</i> field and the operating system minor version is specified by the <i>OSMinorVersion</i> field.

For information about retrieving an <a href="devinst.inf_ddinstall_section">INF DDInstall section</a> for a device, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff551039">SetupDiGetActualSectionToInstall</a>.




## -see-also




<a href="devinst.inf_ddinstall_section">INF DDInstall Section</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552338">SP_ALTPLATFORM_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551039">SetupDiGetActualSectionToInstall</a>
 

 

