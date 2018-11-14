---
UID: NN:gpmgmt.IGPMConstants
title: IGPMConstants
author: windows-sdk-content
description: The IGPMConstants interface supports methods that retrieve the value of multiple Group Policy Management Console (GPMC) constants. To create a GPMConstants object, call the IGPM::GetConstants method.
old-location: gpmc\igpmconstants.htm
tech.root: GPMC
ms.assetid: e9137167-4a2d-4cc4-940e-20f9991c4187
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GPMConstants, IGPMConstants, IGPMConstants interface [GPMC], IGPMConstants interface [GPMC],described, _win32_igpmconstants, gpmc.igpmconstants, gpmgmt/IGPMConstants
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMConstants
 - GPMConstants
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMConstants interface


## -description


The 
<b>IGPMConstants</b> interface supports methods that retrieve the value of multiple Group Policy Management Console (GPMC) constants. To create a <b>GPMConstants</b> object, call the 
<a href="https://msdn.microsoft.com/ba271dbb-320f-409c-aff4-b7dde57f9062">IGPM::GetConstants</a> method.

The <b>GPMConstants</b> object that implements the 
<b>IGPMConstants</b> interface does not introduce new constants. All the constant values and enumeration types that are returned by the <b>GPMConstants</b> object can be found in either the GPMC header file (Gpmgmt.idl or Gpmgmt.h) or in the GPMC type library that is embedded in the Gpmgmt.dll dynamic-link library. Use the <b>GPMConstants</b> object only if you do not have access to the header or to the type library.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMConstants</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGPMConstants</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMConstants</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">get_SearchhPropertyGPOComputerExtensions</a>
</td>
<td align="left" width="63%">
Retrieves the constant value that corresponds to the <b>gpoComputerExtensions</b> search property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMConstants</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">DestinationOptionByRelativeName</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>GPMDestinationOption</b> of opDestinationByRelativeName.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">DestinationOptionNone</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>GPMDestinationOption</b> of opDestinationNone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">DestinationOptionSameAsSource</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>GPMDestinationOption</b> of opDestinationSameAsSource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">DestinationOptionSet</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>GPMDestinationOption</b> of opDestinationSet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">DoNotUseW2KDC</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>DoNotUseW2KDC</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">DoNotValidateDC</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>DoNotValidateDC</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">EntryTypeComputer</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>GPMEntryType</b> of typeComputer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">EntryTypeGlobalGroup</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>GPMEntryType</b> of typeGlobalGroup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">EntryTypeLocalGroup</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>GPMEntryType</b> of typeLocalGroup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">EntryTypeUNCPath</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>GPMEntryType</b> of typeUNCPath.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">EntryTypeUniversalGroup</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>GPMEntryType</b> of typeUniversalGroup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">EntryTypeUnknown</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>GPMEntryType</b> of typeUnknown.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">EntryTypeUser</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>GPMEntryType</b> of typeUser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">MigrationTableOnly</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>GPM_MIGRATIONTABLE_ONLY</b> constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermGPOApply</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permGPOApply</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermGPOCustom</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permGPOCustom</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermGPOEdit</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permGPOEdit</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermGPOEditSecurityAndDelete</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permGPOEditSecurityAndDelete</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermGPORead</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permGPORead</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermSOMGPOCreate</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permSOMGPOCreate</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermSOMLink</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permSOMLink</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermSOMLogging</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permSOMLogging</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermSOMPlanning</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permSOMPlanning</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermSOMWMICreate</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permSOMWMICreate</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermSOMWMIFullControl</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permSOMWMIFullControl</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermWMIFilterCustom</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permWMIFilterCustom</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermWMIFilterEdit</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permWMIFilterEdit</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">PermWMIFilterFullControl</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>permWMIFilterFullControl</b> permission type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">ProcessSecurity</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>GPM_PROCESS_SECURITY</b> constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">ReportHTML</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>ReportHTML</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">ReportXML</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>ReportXML</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">RsopLoggingNoComputer</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>RSOP_NO_USER</b> constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">RsopLoggingNoUser</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>RSOP_NO_USER</b> constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">RSOPModeLogging</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>RSOPModeLogging</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">RSOPModePlanning</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>RSOPModePlanning</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">RSOPModeUnknown</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>RSOPModeUnknown</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">RsopPlanningAssumeCompWQLFilterTrue</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>RSOP_PLANNING_ASSUME_COMP_WQLFILTER_TRUE</b> constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">RsopPlanningAssumeSlowLink</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>RSOP_PLANNING_ASSUME_SLOW_LINK</b> constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">RsopPlanningAssumeUserWQLFilterTrue</a>


</td>
<td align="left" width="63%">
Value that corresponds to the <b>RSOP_PLANNING_ASSUME_USER_WQLFILTER_TRUE</b> constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">RsopPlanningLoopbackOption</a>


</td>
<td align="left" width="63%">
If <i>vbMerge</i> is <b>VARIANT_TRUE</b>, <i>pval</i> corresponds to the <b>RSOP_PLANNING_ASSUME_LOOPBACK_MERGE</b> constant.  If <i>vbMerge</i> is <b>VARIANT_FALSE</b>, <i>pval</i> corresponds to the <b>RSOP_PLANNING_ASSUME_LOOPBACK_REPLACE</b> constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchOpContains</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>opContains</b> search operator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchOpEquals</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>opEquals</b> search operator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchOpNotContains</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>opNotContains</b> search operator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchOpNotEquals</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>opNotEquals</b> search operator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchPropertyBackupMostRecent</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>backupMostRecent</b> search property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchPropertyGPOComputerExtensions</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>gpoComputerExtensions</b> search property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchPropertyGPODisplayName</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>gpoDisplayName</b> search property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchPropertyGPODomain</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>gpoDomain</b> search property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchPropertyGPOEffectivePermissions</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>gpoEffectivePermissions</b> search property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchPropertyGPOID</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>gpoID</b> search property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchPropertyGPOPermissions</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>gpoPermissions</b> search property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchPropertyGPOUserExtensions</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>gpoUserExtensions</b> search property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchPropertyGPOWMIFilter</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>gpoWMIFilter</b> search property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SearchPropertySOMLinks</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>somLinks</b> search property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SecurityFlags</a>


</td>
<td align="left" width="63%">
Represents the portions of the security descriptor that you want to retrieve or set for a Group Policy object (GPO). These values are required to call the 
<a href="https://msdn.microsoft.com/4035119b-2688-4326-8d08-825d53c3d8e2">IGPMGPO::GetSecurityDescriptor</a> and 
<a href="https://msdn.microsoft.com/087cbe19-25d9-4134-8893-1b2906915220">IGPMGPO::SetSecurityDescriptor</a> functions (the <b>GPMGPO.GetSecurityDescriptor</b> and <b>GPMGPO.SetSecurityDescriptor</b> methods).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SOMDomain</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the somDomain scope of management (SOM) type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SOMOU</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the somOU SOM type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">SOMSite</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the somSite SOM type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">UseAnyDC</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>UseAnyDC</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">UsePDC</a>


</td>
<td align="left" width="63%">
Constant value that corresponds to the <b>UsePDC</b> property.

</td>
</tr>
</table> 


## -remarks



Properties that begin with <b>PermGPO</b> apply only to GPOs. Properties that begin with <b>PermWMIFilter</b> apply only to Windows Management Instrumentation (WMI) filters.

For more information about policy-related permissions, see 
<a href="https://msdn.microsoft.com/8da90ca3-1c81-414f-b1a0-a0dfcae745ba">IGPM::CreatePermission</a> (<b>GPM.CreatePermission</b>).




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>
 

 

