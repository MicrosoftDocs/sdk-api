---
UID: NF:faxcomex.IFaxOutboundRouting.GetGroups
title: IFaxOutboundRouting::GetGroups
author: windows-driver-content
description: The IFaxOutboundRouting::GetGroups method retrieves an interface that represents a collection of outbound routing groups.
old-location: fax\_mfax_faxoutboundrouting_getgroups_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8j1v_cpp.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: GetGroups, GetGroups method [Fax Service], GetGroups method [Fax Service],IFaxOutboundRouting interface, IFaxOutboundRouting interface [Fax Service],GetGroups method, IFaxOutboundRouting.GetGroups, IFaxOutboundRouting::GetGroups, _mfax_faxoutboundrouting.getgroups_cpp, fax._mfax_faxoutboundrouting_getgroups_cpp, faxcomex/IFaxOutboundRouting::GetGroups
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
-	IFaxOutboundRouting.GetGroups
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutboundRouting::GetGroups


## -description


The <b>IFaxOutboundRouting::GetGroups</b> method retrieves an interface that represents a collection of outbound routing groups.


## -parameters




### -param pFaxOutboundRoutingGroups [out, retval]

Type: <b><a href="https://msdn.microsoft.com/cf36787b-cc8e-48a8-b81d-5406cbc4bcc8">IFaxOutboundRoutingGroups</a>**</b>

An address of a pointer that receives an <a href="https://msdn.microsoft.com/cf36787b-cc8e-48a8-b81d-5406cbc4bcc8">IFaxOutboundRoutingGroups</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/47e35e11-b288-47c6-bfed-3af7716e7d6b">IFaxOutboundRouting</a>



<a href="https://msdn.microsoft.com/5a05df3b-c56b-4dfc-a0ee-7f1c2861e9ae">Visual Basic Example</a>
 

 

