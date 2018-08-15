---
UID: NN:wmsdkidl.IWMDRMReader
title: IWMDRMReader
author: windows-sdk-content
description: The IWMDRMReader interface provides methods to configure the DRM component and to manage DRM license acquisition and individualization of client applications.
old-location: wmformat\iwmdrmreader.htm
old-project: wmformat
ms.assetid: bf4ff0f3-1f78-43c4-be4d-c74209176e58
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMDRMReader, IWMDRMReader interface [windows Media Format], IWMDRMReader interface [windows Media Format],described, IWMDRMReaderInterface, wmformat.iwmdrmreader, wmsdkidl/IWMDRMReader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMDRMReader
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMReader interface


## -description


<p class="CCE_Message">[<b>IWMDRMReader</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>IWMDRMReader</b> interface provides methods to configure the DRM component and to manage <a href="wmformat_glossary.htm">DRM</a> license acquisition and individualization of client applications. It is used only for content protected using DRM version 7, not the earlier DRM version 1.

This interface can be obtained from a reader object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDRMReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDRMReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDRMReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/757e0926-81aa-48f2-9820-67c8dd51579d">AcquireLicense</a>
</td>
<td align="left" width="63%">
Begins the license acquisition process for a DRM version 7 license.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/837d6fee-d5ba-49d8-ac69-e8ff010a787d">CancelIndividualization</a>
</td>
<td align="left" width="63%">
Cancels a current call to the <b>Individualize</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6a416d1-0bad-49e0-91ad-19e9ff544a8a">CancelLicenseAcquisition</a>
</td>
<td align="left" width="63%">
Cancels a current call to the <b>AcquireLicense</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d33f727-9213-4744-bf65-42b971e3f7da">CancelMonitorLicenseAcquisition</a>
</td>
<td align="left" width="63%">
Cancels a current call to the <b>MonitorLicenseAcquisition</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86ee18be-38a9-4f76-810c-e33281df8c23">GetDRMProperty</a>
</td>
<td align="left" width="63%">
Retrieves <a href="wmformat_glossary.htm">DRM</a>-specific file attributes or run-time properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51bf9aa0-4c96-4c0b-8e5e-b63fd20dcc4d">Individualize</a>
</td>
<td align="left" width="63%">
Individualizes the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b15dce6-7591-479a-b28e-5006418a1c7b">MonitorLicenseAcquisition</a>
</td>
<td align="left" width="63%">
In non-silent license acquisition, informs the application when a license has been successfully acquired.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52f606c2-a746-488f-bbf7-0d0e54b89bf9">SetDRMProperty</a>
</td>
<td align="left" width="63%">
Sets the DRM_Rights that will be requested for the next file that is opened.

</td>
</tr>
</table> 

For information on other interfaces that can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/222ef91c-b776-4de8-b1ad-88c2beca05aa">DRM Attribute List</a>



<a href="https://msdn.microsoft.com/862fc8bc-6e40-4496-862a-c12c8a382116">DRM Properties</a>



<a href="https://msdn.microsoft.com/c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092">Digital Rights Management Features</a>



<a href="https://msdn.microsoft.com/9fb7bbeb-d35f-41f7-b39a-2e5a102b5c05">IWMDRMReader2 Interface</a>



<a href="https://msdn.microsoft.com/9474e06a-9519-456c-b304-efc875a4accc">IWMDRMReader3 Interface</a>



<a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

