---
UID: NN:photoacquire.IPhotoAcquireSettings
title: IPhotoAcquireSettings (photoacquire.h)
author: windows-sdk-content
description: The IPhotoAcquireSettings interface is used to work with image acquisition settings, such as file name format.
old-location: picacq\iphotoacquiresettings.htm
tech.root: acquisition
ms.assetid: c86d0c97-f9ef-4a73-865b-8aea7972193b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPhotoAcquireSettings, IPhotoAcquireSettings interface [Picture Acquisition], IPhotoAcquireSettings interface [Picture Acquisition],described, IPhotoAcquireSettingsInterface, photoacquire/IPhotoAcquireSettings, picacq.iphotoacquiresettings
ms.topic: interface
req.header: photoacquire.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - photoacquire.h
api_name:
 - IPhotoAcquireSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireSettings interface


## -description



The <code>IPhotoAcquireSettings</code> interface is used to work with image acquisition settings, such as file name format.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquireSettings</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPhotoAcquireSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPhotoAcquireSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0acafc4d-e4f5-4dce-a192-18d27024ad83">GetAcquisitionTime</a>
</td>
<td align="left" width="63%">
Retrieves the acquisition time of the current session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35c5c119-52dc-4bf7-a602-8aa0e0781820">GetDateTakenDelta</a>
</td>
<td align="left" width="63%">
Retrieves a length of time to add to or subtract from the acquisition time. Not implemented in this release.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82c82bd9-bd9d-42a0-8723-21d2bf0fb956">GetDeleteAcquiredItems</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether items are to be deleted from the device after transfer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ed9183b-c1a2-4251-bb65-bd947c2034ad">GetFlags</a>
</td>
<td align="left" width="63%">
Retrieves the photo acquire flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e65c5b2-ea1c-4376-a4bb-afbad7efb5ed">GetGroupTag</a>
</td>
<td align="left" width="63%">
Retrieves a tag string for the group of files being downloaded from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca36e3f9-74ad-4704-adeb-d3102668da30">GetOutputFilenameTemplate</a>
</td>
<td align="left" width="63%">
Retrieves a format string (template) that specifies the format of file names.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d19a103e-0f5a-493d-a515-21d8730e39e3">GetSequencePaddingWidth</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating how wide sequential fields in file names will be.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72dc052a-bf8e-4876-8ab6-d0f6857941d5">GetSequenceZeroPadding</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether zeros or spaces will be used to pad sequential file names.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7459792f-20f8-4449-96c5-8c289b17db68">InitializeFromRegistry</a>
</td>
<td align="left" width="63%">
Specifies a registry key from which to initialize settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc43be78-f35b-4159-a15c-c21cddee6c9e">SetAcquisitionTime</a>
</td>
<td align="left" width="63%">
Sets the acquisition time explicitly.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a1f7114-fcd5-41f7-8cbd-f2fef1797418">SetDateTakenDelta</a>
</td>
<td align="left" width="63%">
Sets the time interval to add to or subtract from the "Date Taken" property of each acquired file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f9e760f-35c2-4ca2-89eb-7d6fea8d90ed">SetDeleteAcquiredItems</a>
</td>
<td align="left" width="63%">
Sets a value indicating whether acquired items are to be deleted from the device after transfer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aebe06d8-c764-4d2d-9bd2-58fd9e3714bd">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the photo acquire flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3c8b7dc-5701-412a-a376-498c40017d8f">SetGroupTag</a>
</td>
<td align="left" width="63%">
Sets the group tag for an acquisition session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28eaeee4-05eb-4d51-9e21-937481bc7703">SetOutputFilenameTemplate</a>
</td>
<td align="left" width="63%">
Sets a format string (template) that specifies the format of filenames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c90c109-1522-4722-a691-6f0f3caa50ec">SetSequencePaddingWidth</a>
</td>
<td align="left" width="63%">
Sets a value indicating how wide sequential fields in filenames will be.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5010a61f-a01c-4dd9-850e-581a62b31ab4">SetSequenceZeroPadding</a>
</td>
<td align="left" width="63%">
Sets a value indicating whether zeros or spaces are used to pad file names.

</td>
</tr>
</table> 

