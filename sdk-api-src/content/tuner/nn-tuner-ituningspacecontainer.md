---
UID: NN:tuner.ITuningSpaceContainer
title: ITuningSpaceContainer
author: windows-sdk-content
description: The ITuningSpaceContainer interface is implemented on the SystemTuningSpaces object.
old-location: mstv\ituningspacecontainer.htm
old-project: mstv
ms.assetid: 8f053c53-2a2b-4d98-a510-c516faa21611
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ITuningSpaceContainer, ITuningSpaceContainer interface [Microsoft TV Technologies], ITuningSpaceContainer interface [Microsoft TV Technologies],described, ITuningSpaceContainerInterface, mstv.ituningspacecontainer, tuner/ITuningSpaceContainer
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpaceContainer interface


## -description


The <b>ITuningSpaceContainer</b> interface is implemented on the <a href="https://msdn.microsoft.com/57cdd437-6219-4a72-96d9-642ff79d5879">SystemTuningSpaces</a> object. It provides access to all tuning spaces installed on the host system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITuningSpaceContainer</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITuningSpaceContainer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f31be8f8-3482-484a-b1a3-f27f3e0f7203">_TuningSpacesForCLSID</a>
</td>
<td align="left" width="63%">
Retrieves a collection of tuning spaces that match the specified CLSID. (For use by C++ clients.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds a new persistent tuning space to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99ac47b4-4adc-4e12-b465-4db8ae20ff6d">FindID</a>
</td>
<td align="left" width="63%">
Retrieves the ID of a specified tuning space within the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2bcd80b-b36c-44b1-9a87-beda7ae12117">get__NewEnum</a>
</td>
<td align="left" width="63%">
Enumeration method to support For...Each loops in Automation clients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dfa7700-fef5-4e97-855b-0670cc380af0">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of tuning spaces currently available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cd6a691-8c47-4c26-8afd-57f6965246ff">get_EnumTuningSpaces</a>
</td>
<td align="left" width="63%">
Retrieves a collection of all tuning spaces available on the local system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02e17867-dc72-481a-8693-68e9b0288bba">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a tuning space with the specified ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72692bc6-a210-4e60-9c04-14a7ea531cb4">get_MaxCount</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of tuning spaces allowed on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44e82ec9-ffd0-4bc9-88da-b6c135cbd98f">put_Item</a>
</td>
<td align="left" width="63%">
Saves changes to an existing tuning space in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a469557b-c01a-4922-99ad-641c74130cc9">put_MaxCount</a>
</td>
<td align="left" width="63%">
Sets the maximum number of tuning spaces allowed on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Permanently removes a tuning space from the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f31be8f8-3482-484a-b1a3-f27f3e0f7203">TuningSpacesForCLSID</a>
</td>
<td align="left" width="63%">
Retrieves a collection of tuning spaces that match the specified CLSID string. (For use by Automation clients.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de16a50e-7f5d-41e5-a17f-bb6d97179e4e">TuningSpacesForName</a>
</td>
<td align="left" width="63%">
Retrieves a collection of tuning spaces that match the specified name.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuningSpaceContainer)</code>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

