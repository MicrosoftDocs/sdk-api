---
UID: NN:vsmgmt.IVssEnumMgmtObject
title: IVssEnumMgmtObject
author: windows-sdk-content
description: Contains methods to iterate over and perform other operations on a list of enumerated objects.
old-location: base\ivssenummgmtobject.htm
tech.root: VSS
ms.assetid: c2067822-1824-4676-8376-7d83fcbbaea3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVssEnumMgmtObject, IVssEnumMgmtObject interface [Files], IVssEnumMgmtObject interface [Files],described, base.ivssenummgmtobject, vsmgmt/IVssEnumMgmtObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsMgmt.h
api_name:
 - IVssEnumMgmtObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssEnumMgmtObject interface


## -description


The <b>IVssEnumMgmtObject</b> interface contains 
    methods to iterate over and perform other operations on a list of enumerated objects.

The calling application is responsible for calling 
    <a href="_com_iunknown_release">IUnknown::Release</a> to release the resources held by the 
    returned <b>IVssEnumMgmtObject</b> when it is no longer 
    needed. It may also need to call <b>IUnknown::Release</b> to 
    release temporary objects (such as strings) returned during enumeration.

The 
    <a href="https://msdn.microsoft.com/1203d6de-b389-4349-a83c-5ee729add03c">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot</a>, 
    <a href="https://msdn.microsoft.com/381f8a4a-c88f-4bd3-bff1-6828fe034e66">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForVolume</a>, 
    <a href="https://msdn.microsoft.com/6d9853d3-9c00-47e6-99e8-e499dea9b495">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasOnVolume</a>, and 
    <a href="https://msdn.microsoft.com/2aad75e3-0228-4cc4-b813-c70a7ebfdea5">IVssDifferentialSoftwareSnapshotMgmt::QueryVolumesSupportedForDiffAreas</a> 
    methods return an <b>IVssEnumMgmtObject</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssEnumMgmtObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssEnumMgmtObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssEnumMgmtObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f957052a-5511-4f00-b864-1f03ead2ba58">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the specified list of enumerated elements by creating a copy of the 
    <b>IVssEnumMgmtObject</b> enumerator object.</p> (Inherited from <b>IVssEnumMgmtObject</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ddcf25d-dc3e-4522-a98e-98d867230d42">Next</a>
</td>
<td align="left" width="63%">
Returns the specified number of objects from the specified list of enumerated 
     objects.</p> (Inherited from <b>IVssEnumMgmtObject</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57f984da-6c20-405b-883b-6e54e4ac9546">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator so that 
     <b>IVssEnumMgmtObject</b> starts at the first enumerated 
     object.</p> (Inherited from <b>IVssEnumMgmtObject</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec53ac62-deb3-46f3-947a-1f6a4add4db2">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of objects.</p> (Inherited from <b>IVssEnumMgmtObject</b>)</td>
</tr>
</table> 


## -see-also




<a href="_com_iunknown">IUnknown</a>



<a href="https://msdn.microsoft.com/1203d6de-b389-4349-a83c-5ee729add03c">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot</a>



<a href="https://msdn.microsoft.com/381f8a4a-c88f-4bd3-bff1-6828fe034e66">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForVolume</a>



<a href="https://msdn.microsoft.com/6d9853d3-9c00-47e6-99e8-e499dea9b495">IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasOnVolume</a>



<a href="https://msdn.microsoft.com/2aad75e3-0228-4cc4-b813-c70a7ebfdea5">IVssDifferentialSoftwareSnapshotMgmt::QueryVolumesSupportedForDiffAreas</a>



<a href="https://msdn.microsoft.com/3a0c60df-666c-4e33-a54c-7fa5ddbfde13">Volume Shadow Copy API Interfaces</a>
 

 

