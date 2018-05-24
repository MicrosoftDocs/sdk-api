---
UID: NF:faxcomex.IFaxOutboundRoutingGroups.Add
title: IFaxOutboundRoutingGroups::Add
author: windows-driver-content
description: The IFaxOutboundRoutingGroups::Add method adds an outbound routing group to the collection represented by the IFaxOutboundRoutingGroups interface.
old-location: fax\_mfax_faxoutboundroutinggroups_add_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_35r8_cpp.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],IFaxOutboundRoutingGroups interface, IFaxOutboundRoutingGroups interface [Fax Service],Add method, IFaxOutboundRoutingGroups.Add, IFaxOutboundRoutingGroups::Add, _mfax_faxoutboundroutinggroups.add_cpp, fax._mfax_faxoutboundroutinggroups_add_cpp, faxcomex/IFaxOutboundRoutingGroups::Add
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxOutboundRoutingGroups.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutboundRoutingGroups::Add


## -description


The <b>IFaxOutboundRoutingGroups::Add</b> method adds an outbound routing group to the collection represented by the <a href="https://msdn.microsoft.com/cf36787b-cc8e-48a8-b81d-5406cbc4bcc8">IFaxOutboundRoutingGroups</a> interface.


## -parameters




### -param bstrName [in]

Type: <b>BSTR</b>

Null-terminated string that indicates the name of the group to add. Note that you cannot add the special <b>All Devices</b> routing group.


### -param pFaxOutboundRoutingGroup [out, retval]

Type: <b><a href="https://msdn.microsoft.com/147fbebd-0000-4a24-b9cf-da4132b46edf">IFaxOutboundRoutingGroup</a>**</b>

Address of a pointer that receives a <a href="https://msdn.microsoft.com/147fbebd-0000-4a24-b9cf-da4132b46edf">IFaxOutboundRoutingGroup</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/cf36787b-cc8e-48a8-b81d-5406cbc4bcc8">IFaxOutboundRoutingGroups</a>



<a href="https://msdn.microsoft.com/5a05df3b-c56b-4dfc-a0ee-7f1c2861e9ae">Visual Basic Example</a>
 

 

