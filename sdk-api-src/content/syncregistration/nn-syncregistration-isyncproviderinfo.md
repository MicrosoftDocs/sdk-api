---
UID: NN:syncregistration.ISyncProviderInfo
title: ISyncProviderInfo (syncregistration.h)
author: windows-sdk-content
description: Represents the information and properties needed to create an instance of a synchronization provider.
old-location: winsync\isyncproviderinfo.htm
tech.root: winsync
ms.assetid: fe50e34c-6499-4c1e-b891-7b4f797510f2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncProviderInfo, ISyncProviderInfo interface [Windows Sync], ISyncProviderInfo interface [Windows Sync],described, syncregistration/ISyncProviderInfo, winsync.isyncproviderinfo
ms.topic: interface
f1_keywords: 
 - "syncregistration/ISyncProviderInfo"
req.header: syncregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Syncregistration.h
api_name:
 - ISyncProviderInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncProviderInfo interface


## -description


Represents the information and properties needed to create an instance of a synchronization provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncProviderInfo</b> interface inherits from <b>IPropertyStore</b>. <b>ISyncProviderInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncProviderInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderinfo-getsyncprovider">GetSyncProvider</a>
</td>
<td align="left" width="63%">
Creates an instance of the synchronization provider.

</td>
</tr>
</table> 


## -remarks



This interface is created from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration</a> interface and then subsequently registered.  It is the mechanism by which applications can set the context and UX properties for a synchronization provider by first retrieving the property store and then modifying it.

The properties that are set in  <b>ISyncProviderInfo</b> are written to the registration store by calling the <b>ISyncProviderInfo::Commit</b> method inherited from the <b>IPropertyStore</b> interface. For an example of this, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/overview-of-registering-a-synchronization-provider">Overview of Registering a Synchronization Provider</a>.

You can get and set the properties of a  synchronization provider by calling the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderinfo-getsyncprovider">GetSyncProvider</a> method and manipulating the provider's <b>IPropertyStore</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/overview-of-registering-a-synchronization-provider">Overview of Registering a Synchronization Provider</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-registration-reference">Windows Sync Registration Reference</a>
 

 

