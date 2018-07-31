---
UID: NN:syncregistration.ISyncProviderInfo
title: ISyncProviderInfo
author: windows-sdk-content
description: Represents the information and properties needed to create an instance of a synchronization provider.
old-location: winsync\isyncproviderinfo.htm
old-project: winsync
ms.assetid: fe50e34c-6499-4c1e-b891-7b4f797510f2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISyncProviderInfo, ISyncProviderInfo interface [Windows Sync], ISyncProviderInfo interface [Windows Sync],described, syncregistration/ISyncProviderInfo, winsync.isyncproviderinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: SYNC_REGISTRATION_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - ISyncProviderInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
<a href="https://msdn.microsoft.com/74b70f31-0934-4599-9515-e94b6622d440">GetSyncProvider</a>
</td>
<td align="left" width="63%">
Creates an instance of the synchronization provider.

</td>
</tr>
</table> 


## -remarks



This interface is created from the <a href="https://msdn.microsoft.com/e7cf0c05-9d07-4630-ae34-9a9dd81492b2">ISyncProviderRegistration</a> interface and then subsequently registered.  It is the mechanism by which applications can set the context and UX properties for a synchronization provider by first retrieving the property store and then modifying it.

The properties that are set in  <b>ISyncProviderInfo</b> are written to the registration store by calling the <b>ISyncProviderInfo::Commit</b> method inherited from the <b>IPropertyStore</b> interface. For an example of this, see <a href="https://msdn.microsoft.com/0d496730-a4db-4898-aad9-1b5ca3b8ea51">Overview of Registering a Synchronization Provider</a>.

You can get and set the properties of a  synchronization provider by calling the <a href="https://msdn.microsoft.com/74b70f31-0934-4599-9515-e94b6622d440">GetSyncProvider</a> method and manipulating the provider's <b>IPropertyStore</b>.




## -see-also




<a href="https://msdn.microsoft.com/e7cf0c05-9d07-4630-ae34-9a9dd81492b2">ISyncProviderRegistration Interface</a>



<a href="https://msdn.microsoft.com/0d496730-a4db-4898-aad9-1b5ca3b8ea51">Overview of Registering a Synchronization Provider</a>



<a href="https://msdn.microsoft.com/8233671e-bf89-448d-8347-9b4f0ae7501f">Windows Sync Registration Reference</a>
 

 

