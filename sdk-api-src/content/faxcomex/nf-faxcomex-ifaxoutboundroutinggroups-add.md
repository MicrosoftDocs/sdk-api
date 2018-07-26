---
UID: NF:faxcomex.IFaxOutboundRoutingGroups.Add
title: IFaxOutboundRoutingGroups::Add
author: windows-sdk-content
description: The Add method adds an outbound routing group to the FaxOutboundRoutingGroups collection.
old-location: fax\_mfax_faxoutboundroutinggroups_add.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_35r8.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],FaxOutboundRoutingGroups object, FaxOutboundRoutingGroups object [Fax Service],Add method, FaxOutboundRoutingGroups.Add, IFaxOutboundRoutingGroups.Add, IFaxOutboundRoutingGroups::Add, _mfax_faxoutboundroutinggroups.add, fax._mfax_faxoutboundroutinggroups_add
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxOutboundRoutingGroups.Add
 - IFaxOutboundRoutingGroups.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutboundRoutingGroups::Add


## -description


The <b>Add</b> method adds an outbound routing group to the <a href="https://msdn.microsoft.com/799a034c-c807-428c-8536-bc68dce5cd8e">FaxOutboundRoutingGroups</a> collection.


## -parameters




### -param bstrName

Type: <b>String</b>

Null-terminated string that indicates the name of the group to add. Note that you cannot add the special <b>All Devices</b> routing group.


### -param pFaxOutboundRoutingGroup






#### - FaxOutboundRoutingGroup

Type: <b><a href="https://msdn.microsoft.com/894a58b7-3a5f-4723-abcb-764567e49e76">FaxOutboundRoutingGroup</a>**</b>

A <a href="https://msdn.microsoft.com/894a58b7-3a5f-4723-abcb-764567e49e76">FaxOutboundRoutingGroup</a> object.


## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/799a034c-c807-428c-8536-bc68dce5cd8e">FaxOutboundRoutingGroups</a>



<a href="https://msdn.microsoft.com/cf36787b-cc8e-48a8-b81d-5406cbc4bcc8">IFaxOutboundRoutingGroups</a>



<a href="https://msdn.microsoft.com/5a05df3b-c56b-4dfc-a0ee-7f1c2861e9ae">Visual Basic Example</a>
 

 

