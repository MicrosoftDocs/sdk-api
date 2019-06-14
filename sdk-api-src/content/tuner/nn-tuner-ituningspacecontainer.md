---
UID: NN:tuner.ITuningSpaceContainer
title: ITuningSpaceContainer (tuner.h)
author: windows-sdk-content
description: The ITuningSpaceContainer interface is implemented on the SystemTuningSpaces object.
old-location: mstv\ituningspacecontainer.htm
tech.root: mstv
ms.assetid: 8f053c53-2a2b-4d98-a510-c516faa21611
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITuningSpaceContainer, ITuningSpaceContainer interface [Microsoft TV Technologies], ITuningSpaceContainer interface [Microsoft TV Technologies],described, ITuningSpaceContainerInterface, mstv.ituningspacecontainer, tuner/ITuningSpaceContainer
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - ITuningSpaceContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITuningSpaceContainer interface


## -description


The <b>ITuningSpaceContainer</b> interface is implemented on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/systemtuningspaces-object">SystemTuningSpaces</a> object. It provides access to all tuning spaces installed on the host system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITuningSpaceContainer</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITuningSpaceContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITuningSpaceContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-_tuningspacesforclsid">_TuningSpacesForCLSID</a>
</td>
<td align="left" width="63%">
Retrieves a collection of tuning spaces that match the specified CLSID. (For use by C++ clients.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-add">Add</a>
</td>
<td align="left" width="63%">
Adds a new persistent tuning space to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-findid">FindID</a>
</td>
<td align="left" width="63%">
Retrieves the ID of a specified tuning space within the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Enumeration method to support For...Each loops in Automation clients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of tuning spaces currently available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-get_enumtuningspaces">get_EnumTuningSpaces</a>
</td>
<td align="left" width="63%">
Retrieves a collection of all tuning spaces available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a tuning space with the specified ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-get_maxcount">get_MaxCount</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of tuning spaces allowed on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-put_item">put_Item</a>
</td>
<td align="left" width="63%">
Saves changes to an existing tuning space in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-put_maxcount">put_MaxCount</a>
</td>
<td align="left" width="63%">
Sets the maximum number of tuning spaces allowed on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-remove">Remove</a>
</td>
<td align="left" width="63%">
Permanently removes a tuning space from the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-_tuningspacesforclsid">TuningSpacesForCLSID</a>
</td>
<td align="left" width="63%">
Retrieves a collection of tuning spaces that match the specified CLSID string. (For use by Automation clients.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-tuningspacesforname">TuningSpacesForName</a>
</td>
<td align="left" width="63%">
Retrieves a collection of tuning spaces that match the specified name.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuningSpaceContainer)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

