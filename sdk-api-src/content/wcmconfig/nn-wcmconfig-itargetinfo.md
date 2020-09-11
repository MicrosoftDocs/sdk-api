---
UID: NN:wcmconfig.ITargetInfo
title: ITargetInfo (wcmconfig.h)
description: Defines the offline target information, specifically, file and registry locations as well as wow64 information.
helpviewer_keywords: ["ITargetInfo","ITargetInfo interface [SMI]","ITargetInfo interface [SMI]","described","smi.itargetinfo","wcmconfig/ITargetInfo"]
old-location: smi\itargetinfo.htm
tech.root: SMI
ms.assetid: f1dd3c93-43ca-4804-8330-55acaccf8ea8
ms.date: 12/05/2018
ms.keywords: ITargetInfo, ITargetInfo interface [SMI], ITargetInfo interface [SMI],described, smi.itargetinfo, wcmconfig/ITargetInfo
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITargetInfo
 - wcmconfig/ITargetInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ITargetInfo
---

# ITargetInfo interface


## -description

Defines the offline target information,  specifically, file and registry locations as well as wow64 information.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITargetInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITargetInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITargetInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-expandtarget">ExpandTarget</a>
</td>
<td align="left" width="63%">
Expands a location string to indicate the offline installation location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-expandtargetpath">ExpandTargetPath</a>
</td>
<td align="left" width="63%">
Expands a location string to indicate the offline installation location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-getenumerator">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets the enumerator to access the collection of offline properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Gets a property value for the offline installation location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-getschemahivelocation">GetSchemaHiveLocation</a>
</td>
<td align="left" width="63%">
Get the location of the schema hive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-getschemahivemountname">GetSchemaHiveMountName</a>
</td>
<td align="left" width="63%">
Gets the name of the mount location of the schema hive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-gettargetid">GetTargetID</a>
</td>
<td align="left" width="63%">
Gets a unique identifier associated with the current target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-gettargetmode">GetTargetMode</a>
</td>
<td align="left" width="63%">
Gets the current target mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-gettargetprocessorarchitecture">GetTargetProcessorArchitecture</a>
</td>
<td align="left" width="63%">
Gets processor architecture associated with the current target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-gettemporarystorelocation">GetTemporaryStoreLocation</a>
</td>
<td align="left" width="63%">
Gets the current temporary store location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-loadmodule">LoadModule</a>
</td>
<td align="left" width="63%">
Loads the module from the offline installation location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-setmodulepath">SetModulePath</a>
</td>
<td align="left" width="63%">
Sets the module path for offline installation location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets a property value for the offline installation location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-setschemahivelocation">SetSchemaHiveLocation</a>
</td>
<td align="left" width="63%">
Sets the location of the schema hive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-setschemahivemountname">SetSchemaHiveMountName</a>
</td>
<td align="left" width="63%">
Sets the name of the mount location of the schema hive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-settargetid">SetTargetID</a>
</td>
<td align="left" width="63%">
Sets the unique identifier associated with current target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-settargetmode">SetTargetMode</a>
</td>
<td align="left" width="63%">
Sets the target mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-settargetprocessorarchitecture">SetTargetProcessorArchitecture</a>
</td>
<td align="left" width="63%">
Sets the processor architecture associated with the current target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-settemporarystorelocation">SetTemporaryStoreLocation</a>
</td>
<td align="left" width="63%">
Sets the current temporary store location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-setwow64context">SetWow64Context</a>
</td>
<td align="left" width="63%">
Sets an opaque context object for wow64 redirection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-itargetinfo-translatewow64">TranslateWow64</a>
</td>
<td align="left" width="63%">
Translates paths for wow64 redirection.

</td>
</tr>
</table>

