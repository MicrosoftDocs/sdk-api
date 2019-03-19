---
UID: NF:setupapi.SetupDiGetActualModelsSectionA
title: SetupDiGetActualModelsSectionA function (setupapi.h)
author: windows-sdk-content
description: The SetupDiGetActualModelsSection function retrieves the appropriate decorated INF Models section to use when installing a device from a device INF file.
old-location: devinst\setupdigetactualmodelssection.htm
tech.root: devinst
ms.assetid: 8338989a-ef99-479c-8163-ad8d65eba32b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupDiGetActualModelsSection, SetupDiGetActualModelsSection function [Device and Driver Installation], SetupDiGetActualModelsSectionA, SetupDiGetActualModelsSectionW, devinst.setupdigetactualmodelssection, di-rtns_d008a45e-8dbe-4d59-ac12-be4ac28eebcb.xml, setupapi/SetupDiGetActualModelsSection
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Server 2003 with Service Pack 1 (SP1) and later versions of Windows.
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
req.lib: Setupapi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetActualModelsSection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiGetActualModelsSectionA function


## -description


The <b>SetupDiGetActualModelsSection</b> function retrieves the appropriate decorated <a href="https://msdn.microsoft.com/library/Ff547456(v=VS.85).aspx">INF Models section</a> to use when installing a device from a device INF file.


## -parameters




### -param Context [in]

A pointer to an INF file context that specifies a <i>manufacturer-identifier</i> entry in an <a href="https://msdn.microsoft.com/library/Ff547454(v=VS.85).aspx">INF Manufacturer section</a> of an INF file. The <i>manufacturer-identifier</i> entry specifies an INF <i>Models</i> section name and optionally specifies <i>TargetOSVersion</i> decorations for the <i>Models</i> section name. For information about INF files and an INF file context, see the Platform SDK topics on <a href="http://go.microsoft.com/fwlink/p/?linkid=81350">using INF files</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=81351">INFCONTEXT structure</a>. 


### -param AlternatePlatformInfo [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/d9aba6c9-1b23-4ce0-b796-904b39bec3ac">SP_ALTPLATFORM_INFO</a> structure that supplies information about a Windows version and processor architecture. The <b>cbSize</b> member of this structure must be set to <b>sizeof(</b>SP_ALTPLATFORM_INFO_V2<b>)</b>. This parameter is optional and can be set to <b>NULL</b>.


### -param InfSectionWithExt [out, optional]

A pointer to a buffer that receives a string that contains the decorated INF <i>Models</i> section name and a NULL terminator. If <i>AlternatePlatformInfo</i> is not supplied, the decorated INF <i>Models</i> section name applies to the current platform; otherwise the name applies to the specified alternative platform. This parameter is optional and can be set to <b>NULL</b>. If this parameter is <b>NULL</b>, the function returns <b>TRUE</b> and sets <i>RequiredSize</i> to the size, in characters, that is required to return the decorated <i>Models</i> section name and a terminating NULL character. 


### -param InfSectionWithExtSize [in]

 The size, in characters, of the <i>DecoratedModelsSection </i>buffer. If <i>DecoratedModelsSection</i> is <b>NULL</b>, this parameter must be set to zero.


### -param RequiredSize [out, optional]

A pointer to a DWORD-type variable that receives the size, in characters, of the <i>DecoratedModelsSection</i> buffer that is required to retrieve the decorated <i>Models</i> section name and a terminating NULL character. This parameter is optional and can be set to <b>NULL</b>.


### -param Reserved

Reserved for internal system use. This parameter must be set to <b>NULL</b>.


## -returns



<b>SetupDiGetActualModelsSection</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, the function returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



<b>SetupDiGetActualModelsSection</b> determines which <i>TargetOSVersion</i> fields in the <i>manufacturer-identifier</i> entry (supplied by <i>Context</i>) apply to the current platform, if <i>AlternatePlatformInfo</i> is not supplied, or to an alternative platform, if alternative platform information is supplied. <b>SetupDiGetActualModelsSection</b> selects the most appropriate platform based on all the <i>TargetOSVersion</i> fields, appends the <i>TargetOSVersion</i> string to the INF <i>Models</i> section name, and returns the decorated INF <i>Models</i> section name to the caller. In a <i>manufacturer-identifier</i> entry, the operating system major version is specified by the <i>OSMajorVersion</i> field and the operating system minor version is specified by the <i>OSMinorVersion</i> field.

For information about retrieving an <a href="https://msdn.microsoft.com/library/Ff547344(v=VS.85).aspx">INF DDInstall section</a> for a device, see <a href="https://msdn.microsoft.com/ccb5e1a4-e6c3-48e5-ac25-b9b5504a03d7">SetupDiGetActualSectionToInstall</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Ff547344(v=VS.85).aspx">INF DDInstall Section</a>



<a href="https://msdn.microsoft.com/d9aba6c9-1b23-4ce0-b796-904b39bec3ac">SP_ALTPLATFORM_INFO</a>



<a href="https://msdn.microsoft.com/ccb5e1a4-e6c3-48e5-ac25-b9b5504a03d7">SetupDiGetActualSectionToInstall</a>
 

 

