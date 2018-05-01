---
UID: NN:adomd.ICatalog
title: ICatalog
author: windows-driver-content
description: State object, holds open catalog and all info about catalog
old-location: helpapi\icatalog.htm
old-project: helpapi
ms.assetid: 6d09032b-3311-434b-b8db-97e3ee2f5f67
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ICatalog, ICatalog interface [HelpAPI], ICatalog interface [HelpAPI], described, adomd/ICatalog, helpapi.icatalog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: adomd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Help.Runtime.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	adomd.h
api_name:
-	ICatalog
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICatalog interface


## -description


State object, holds open catalog and all info about catalog


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatalog</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICatalog</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICatalog</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
method Close - closes a currently open catalog

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f2be8ba-886c-4d33-8264-63b056bae9eb">GetReadWriteLock</a>
</td>
<td align="left" width="63%">
Method GetReadWriteLock - Return a reference to the catalog read write lock object for a given location

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3fde805-2d1a-492e-9deb-40aa588fff35">IsLanguageSupportAvailable</a>
</td>
<td align="left" width="63%">
Method IsLanguageSupportAvailable - Check to see if the natural language support is installed on the system for a given language

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
method Open - opens a catalog given a valid catalog directory path and list of prioritized languages for fallback

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13ff1831-8f20-47be-af2d-7b689c5b597f">OpenMshx</a>
</td>
<td align="left" width="63%">
method OpenMshx - opens an MSHX catalog given a valid path to the MSHX file

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatalog</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3f44cecf-3628-4341-baaf-b4f7aebdbcfa">ContentPath</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
property ContentPath - returns the content path for this catalog

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/872f02b9-677a-4c40-ace3-649f9d5fbadf">IsOpen</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns true if a catalog is currently open, else false

</td>
</tr>
</table> 

