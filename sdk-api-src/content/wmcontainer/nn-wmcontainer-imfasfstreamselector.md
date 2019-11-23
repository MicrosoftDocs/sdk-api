---
UID: NN:wmcontainer.IMFASFStreamSelector
title: IMFASFStreamSelector (wmcontainer.h)

description: Selects streams in an Advanced Systems Format (ASF) file, based on the mutual exclusion information in the ASF header.
old-location: mf\imfasfstreamselector.htm
tech.root: medfound
ms.assetid: d2e1fc15-2e12-4698-a4b1-ca8046d228de

ms.date: 12/05/2018
ms.keywords: IMFASFStreamSelector, IMFASFStreamSelector interface [Media Foundation], IMFASFStreamSelector interface [Media Foundation],described, d2e1fc15-2e12-4698-a4b1-ca8046d228de, mf.imfasfstreamselector, wmcontainer/IMFASFStreamSelector
ms.topic: interface
f1_keywords: 
 - "wmcontainer/IMFASFStreamSelector"
dev_langs:
 - c++
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFStreamSelector
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFASFStreamSelector interface


## -description


Selects streams in an Advanced Systems Format (ASF) file, based on the mutual exclusion information in the ASF header. The ASF stream selector object exposes this interface. To create the ASF stream selector, call <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfstreamselector">MFCreateASFStreamSelector</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFStreamSelector</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFASFStreamSelector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFASFStreamSelector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-bitratetostepnumber">BitrateToStepNumber</a>
</td>
<td align="left" width="63%">
Retrieves the index of a bandwidth step that is appropriate for a specified bit rate. This method is used for multiple bit rate (MBR) content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getbandwidthstep">GetBandwidthStep</a>
</td>
<td align="left" width="63%">
Retrieves the stream numbers that apply to a bandwidth step. This method is used for MBR content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getbandwidthstepcount">GetBandwidthStepCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of bandwidth steps that exist for the content. This method is used for MBR content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getoutputcount">GetOutputCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of outputs for the ASF content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getoutputfromstream">GetOutputFromStream</a>
</td>
<td align="left" width="63%">
Retrieves the output number associated with a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getoutputmutex">GetOutputMutex</a>
</td>
<td align="left" width="63%">
Retrieves a mutual exclusion object for an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getoutputmutexcount">GetOutputMutexCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of mutual exclusion objects associated with an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getoutputoverride">GetOutputOverride</a>
</td>
<td align="left" width="63%">
Retrieves the manual output override selection that is set for a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getoutputstreamcount">GetOutputStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of streams associated with an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getoutputstreamnumbers">GetOutputStreamNumbers</a>
</td>
<td align="left" width="63%">
Retrieves the stream numbers for all of the streams that are associated with an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getstreamcount">GetStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of streams that are in the ASF content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-setoutputmutexselection">SetOutputMutexSelection</a>
</td>
<td align="left" width="63%">
Selects a mutual exclusion record to use for a mutual exclusion object associated with an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-setoutputoverride">SetOutputOverride</a>
</td>
<td align="left" width="63%">
Sets the selection status of an output, overriding other selection criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-setstreamselectorflags">SetStreamSelectorFlags</a>
</td>
<td align="left" width="63%">
Sets options for the stream selector.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

