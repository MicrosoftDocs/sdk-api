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


The <b>Add</b> method adds an outbound routing group to the <a href="https://msdn.microsoft.com/library/ms689211(v=VS.85).aspx">FaxOutboundRoutingGroups</a> collection.


## -parameters




### -param bstrName

Type: <b>String</b>

Null-terminated string that indicates the name of the group to add. Note that you cannot add the special <b>All Devices</b> routing group.


### -param pFaxOutboundRoutingGroup






#### - FaxOutboundRoutingGroup

Type: <b><a href="https://msdn.microsoft.com/library/ms689098(v=VS.85).aspx">FaxOutboundRoutingGroup</a>**</b>

A <a href="https://msdn.microsoft.com/library/ms689098(v=VS.85).aspx">FaxOutboundRoutingGroup</a> object.


## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/library/ms689211(v=VS.85).aspx">FaxOutboundRoutingGroups</a>



<a href="https://msdn.microsoft.com/library/ms689212(v=VS.85).aspx">IFaxOutboundRoutingGroups</a>



<a href="https://msdn.microsoft.com/library/ms693408(v=VS.85).aspx">Visual Basic Example</a>
 

 

