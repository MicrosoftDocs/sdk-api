---
UID: NN:photoacquire.IPhotoAcquireSettings
title: IPhotoAcquireSettings (photoacquire.h)
author: windows-sdk-content
description: The IPhotoAcquireSettings interface is used to work with image acquisition settings, such as file name format.
old-location: picacq\iphotoacquiresettings.htm
tech.root: acquisition
ms.assetid: c86d0c97-f9ef-4a73-865b-8aea7972193b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireSettings, IPhotoAcquireSettings interface [Picture Acquisition], IPhotoAcquireSettings interface [Picture Acquisition],described, IPhotoAcquireSettingsInterface, photoacquire/IPhotoAcquireSettings, picacq.iphotoacquiresettings
ms.topic: interface
f1_keywords: ["photoacquire/IPhotoAcquireSettings"]
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
ms.custom: 19H1
---

# IPhotoAcquireSettings interface


## -description



The <code>IPhotoAcquireSettings</code> interface is used to work with image acquisition settings, such as file name format.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquireSettings</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPhotoAcquireSettings</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-getacquisitiontime">GetAcquisitionTime</a>
</td>
<td align="left" width="63%">
Retrieves the acquisition time of the current session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//dd370746(v=vs.85)">GetDateTakenDelta</a>
</td>
<td align="left" width="63%">
Retrieves a length of time to add to or subtract from the acquisition time. Not implemented in this release.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//dd370747(v=vs.85)">GetDeleteAcquiredItems</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether items are to be deleted from the device after transfer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Retrieves the photo acquire flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-getgrouptag">GetGroupTag</a>
</td>
<td align="left" width="63%">
Retrieves a tag string for the group of files being downloaded from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-getoutputfilenametemplate">GetOutputFilenameTemplate</a>
</td>
<td align="left" width="63%">
Retrieves a format string (template) that specifies the format of file names.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-getsequencepaddingwidth">GetSequencePaddingWidth</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating how wide sequential fields in file names will be.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-getsequencezeropadding">GetSequenceZeroPadding</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether zeros or spaces will be used to pad sequential file names.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-initializefromregistry">InitializeFromRegistry</a>
</td>
<td align="left" width="63%">
Specifies a registry key from which to initialize settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setacquisitiontime">SetAcquisitionTime</a>
</td>
<td align="left" width="63%">
Sets the acquisition time explicitly.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//dd370755(v=vs.85)">SetDateTakenDelta</a>
</td>
<td align="left" width="63%">
Sets the time interval to add to or subtract from the "Date Taken" property of each acquired file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//dd370756(v=vs.85)">SetDeleteAcquiredItems</a>
</td>
<td align="left" width="63%">
Sets a value indicating whether acquired items are to be deleted from the device after transfer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the photo acquire flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setgrouptag">SetGroupTag</a>
</td>
<td align="left" width="63%">
Sets the group tag for an acquisition session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setoutputfilenametemplate">SetOutputFilenameTemplate</a>
</td>
<td align="left" width="63%">
Sets a format string (template) that specifies the format of filenames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setsequencepaddingwidth">SetSequencePaddingWidth</a>
</td>
<td align="left" width="63%">
Sets a value indicating how wide sequential fields in filenames will be.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setsequencezeropadding">SetSequenceZeroPadding</a>
</td>
<td align="left" width="63%">
Sets a value indicating whether zeros or spaces are used to pad file names.

</td>
</tr>
</table> 

