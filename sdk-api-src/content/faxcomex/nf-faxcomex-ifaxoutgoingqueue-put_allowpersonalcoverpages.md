---
UID: NF:faxcomex.IFaxOutgoingQueue.put_AllowPersonalCoverPages
title: IFaxOutgoingQueue::put_AllowPersonalCoverPages
author: windows-sdk-content
description: The AllowPersonalCoverPages property is a Boolean value that indicates whether fax client applications can include a user-designed cover page with fax transmissions.
old-location: fax\_mfax_faxoutgoingqueue_allowpersonalcoverpages_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5cc3.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: AllowPersonalCoverPages property [Fax Service], AllowPersonalCoverPages property [Fax Service],FaxOutgoingQueue object, FaxOutgoingQueue object [Fax Service],AllowPersonalCoverPages property, FaxOutgoingQueue.AllowPersonalCoverPages, IFaxOutgoingQueue.put_AllowPersonalCoverPages, IFaxOutgoingQueue::put_AllowPersonalCoverPages, _mfax_faxoutgoingqueue.allowpersonalcoverpages, fax._mfax_faxoutgoingqueue_allowpersonalcoverpages, fax._mfax_faxoutgoingqueue_allowpersonalcoverpages_vb, put_AllowPersonalCoverPages
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
 - FaxOutgoingQueue.AllowPersonalCoverPages
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingQueue::put_AllowPersonalCoverPages


## -description


The AllowPersonalCoverPages property is a Boolean value that indicates whether fax client applications can include a user-designed cover page with fax transmissions.

This property is read/write.


## -parameters


## -remarks



If this property is equal to <b>True</b>, clients can include personal cover page files with fax transmissions. If this property is equal to <b>False</b>, clients must use a common cover page file stored on the fax server. 

To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/library/ms687528(v=VS.85).aspx">FaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/library/ms687529(v=VS.85).aspx">IFaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/library/ms692914(v=VS.85).aspx">Setting the Outgoing Queue Properties</a>
 

 

