---
UID: NN:appxpackaging.IAppxManifestReader
title: IAppxManifestReader (appxpackaging.h)
description: Represents an object model of the package manifest that provides methods to access manifest elements and attributes.
helpviewer_keywords: ["IAppxManifestReader","IAppxManifestReader interface [App packaging and management]","IAppxManifestReader interface [App packaging and management]","described","appxpackaging/IAppxManifestReader","appxpkg.iappxmanifestreader"]
old-location: appxpkg\iappxmanifestreader.htm
tech.root: appxpkg
ms.assetid: 3DA45F2F-7088-4A9B-968C-91E402CAA412
ms.date: 12/05/2018
ms.keywords: IAppxManifestReader, IAppxManifestReader interface [App packaging and management], IAppxManifestReader interface [App packaging and management],described, appxpackaging/IAppxManifestReader, appxpkg.iappxmanifestreader
f1_keywords:
- appxpackaging/IAppxManifestReader
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- AppxPackaging.h
api_name:
- IAppxManifestReader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxManifestReader interface


## -description


Represents an object model of the package manifest that provides methods to access manifest elements and attributes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestReader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestReader</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getapplications">GetApplications</a>
</td>
<td align="left" width="63%">
Gets an enumerator that iterates through the applications defined in the manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getcapabilities">GetCapabilities</a>
</td>
<td align="left" width="63%">
Gets the list of capabilities requested by the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getdevicecapabilities">GetDeviceCapabilities</a>
</td>
<td align="left" width="63%">
Gets an enumerator that iterates through the device capabilities defined in the manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getpackagedependencies">GetPackageDependencies</a>
</td>
<td align="left" width="63%">
Gets an enumerator that iterates through dependencies defined in the manifest. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getpackageid">GetPackageId</a>
</td>
<td align="left" width="63%">
Gets the package identifier defined in the manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getprerequisite">GetPrerequisite</a>
</td>
<td align="left" width="63%">
Gets the specified prerequisite as defined in the package manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Gets the properties of the package as defined in the manifest. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getresources">GetResources</a>
</td>
<td align="left" width="63%">
Gets an enumerator that iterates through the resources defined in the manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Gets the raw XML parsed and read by the manifest reader.

</td>
</tr>
</table> 


## -remarks



Do  not implement this object. Use the provided implementation instead.

This <b>IAppxManifestReader</b> object parses and validates the app package manifest and exposes elements and attributes in the manifest in a type-safe manner. This object can also be used to get an underlying <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> for the raw XML if needed.

<div class="alert"><b>Note</b>  Starting with Windows 8.1, we recommend not to use <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getresources">IAppxManifestReader::GetResources</a> anymore to only iterate over the <b>Language</b> values in the manifest. Instead, use <b>IAppxManifestReader2::GetResources</b> because it iterates over other resource qualifiers as well, such as, <b>Scale</b> and <b>DXFeatureLevel</b>. </div>
<div> </div>
This object can be retrieved using the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory-createmanifestreader">CreateManifestReader</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory">IAppxFactory</a> interface or the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getmanifest">GetManifest</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagereader">IAppxPackageReader</a> interface. In either case, the manifest is validated before returning the <b>IAppxManifestReader</b> object. If the XML is not syntactically valid, then the above mentioned methods fail, and the <b>IAppxManifestReader</b> object is not returned.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_capabilities">APPX_CAPABILITIES</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestapplicationsenumerator">IAppxManifestApplicationsEnumerator</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestdevicecapabilitiesenumerator">IAppxManifestDeviceCapabilitiesEnumerator</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackagedependenciesenumerator">IAppxManifestPackageDependenciesEnumerator</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackageid">IAppxManifestPackageId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestproperties">IAppxManifestProperties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestresourcesenumerator">IAppxManifestResourcesEnumerator</a>
 

 

