---
UID: NN:appxpackaging.IAppxManifestReader
title: IAppxManifestReader
author: windows-sdk-content
description: Represents an object model of the package manifest that provides methods to access manifest elements and attributes.
old-location: appxpkg\iappxmanifestreader.htm
old-project: appxpkg
ms.assetid: 3DA45F2F-7088-4A9B-968C-91E402CAA412
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxManifestReader, IAppxManifestReader interface [App packaging and management], IAppxManifestReader interface [App packaging and management],described, appxpackaging/IAppxManifestReader, appxpkg.iappxmanifestreader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxManifestReader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestReader interface


## -description


Represents an object model of the package manifest that provides methods to access manifest elements and attributes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EC575692-93D6-43F1-857B-9A27DD50B8FC">GetApplications</a>
</td>
<td align="left" width="63%">
Gets an enumerator that iterates through the applications defined in the manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451391">GetCapabilities</a>
</td>
<td align="left" width="63%">
Gets the list of capabilities requested by the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06257DB1-992E-4A8D-8221-76DA3DF0FA1F">GetDeviceCapabilities</a>
</td>
<td align="left" width="63%">
Gets an enumerator that iterates through the device capabilities defined in the manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C40276CC-8F97-4DCF-A5C4-193453B8FA02">GetPackageDependencies</a>
</td>
<td align="left" width="63%">
Gets an enumerator that iterates through dependencies defined in the manifest. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67E1B1A4-E934-4CCF-AF94-A7923B192A21">GetPackageId</a>
</td>
<td align="left" width="63%">
Gets the package identifier defined in the manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1CF44513-AA07-4591-9134-A156A538C8F1">GetPrerequisite</a>
</td>
<td align="left" width="63%">
Gets the specified prerequisite as defined in the package manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991811">GetProperties</a>
</td>
<td align="left" width="63%">
Gets the properties of the package as defined in the manifest. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451131">GetResources</a>
</td>
<td align="left" width="63%">
Gets an enumerator that iterates through the resources defined in the manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00467E92-5282-4119-A036-00CE769839B9">GetStream</a>
</td>
<td align="left" width="63%">
Gets the raw XML parsed and read by the manifest reader.

</td>
</tr>
</table> 


## -remarks



Do  not implement this object. Use the provided implementation instead.

This <b>IAppxManifestReader</b> object parses and validates the app package manifest and exposes elements and attributes in the manifest in a type-safe manner. This object can also be used to get an underlying <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> for the raw XML if needed.

<div class="alert"><b>Note</b>  Starting with Windows 8.1, we recommend not to use <a href="https://msdn.microsoft.com/2F0109C2-99F5-4AEE-9596-153764FA8FA3">IAppxManifestReader::GetResources</a> anymore to only iterate over the <b>Language</b> values in the manifest. Instead, use <b>IAppxManifestReader2::GetResources</b> because it iterates over other resource qualifiers as well, such as, <b>Scale</b> and <b>DXFeatureLevel</b>. </div>
<div> </div>
This object can be retrieved using the <a href="https://msdn.microsoft.com/BF6C83FF-8CB1-47C0-84C3-E71059F0796E">CreateManifestReader</a> method of the <a href="https://msdn.microsoft.com/4EA79D44-7C26-4B65-81A1-394E1E540F34">IAppxFactory</a> interface or the <a href="https://msdn.microsoft.com/5EE69CCD-C941-4346-B539-C415CE9EA1FB">GetManifest</a> method of the <a href="https://msdn.microsoft.com/D34D0909-BE2B-4182-8C3D-36A4E8DDC820">IAppxPackageReader</a> interface. In either case, the manifest is validated before returning the <b>IAppxManifestReader</b> object. If the XML is not syntactically valid, then the above mentioned methods fail, and the <b>IAppxManifestReader</b> object is not returned.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4912BCB0-424B-40F9-BBD1-3AD0A60B3320">APPX_CAPABILITIES</a>



<a href="https://msdn.microsoft.com/49955DE0-A6BE-4FD7-B8E3-E4126B3C4B8F">IAppxManifestApplicationsEnumerator</a>



<a href="https://msdn.microsoft.com/6A544E15-BB92-48C3-963D-789B04464277">IAppxManifestDeviceCapabilitiesEnumerator</a>



<a href="https://msdn.microsoft.com/A09709AE-301F-4457-8E02-1A88FB283A43">IAppxManifestPackageDependenciesEnumerator</a>



<a href="https://msdn.microsoft.com/8665AC2B-4D06-4684-99B1-E22533CA04AA">IAppxManifestPackageId</a>



<a href="https://msdn.microsoft.com/5DA0A805-13D3-4977-8EFB-45E8B51AAF60">IAppxManifestProperties</a>



<a href="https://msdn.microsoft.com/D76C7512-962F-4AFE-934F-BBC215B5FE99">IAppxManifestResourcesEnumerator</a>
 

 

