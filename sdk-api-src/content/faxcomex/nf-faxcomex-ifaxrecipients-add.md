---
UID: NF:faxcomex.IFaxRecipients.Add
title: IFaxRecipients::Add
author: windows-sdk-content
description: The Add method adds a new FaxRecipient object to the FaxRecipients collection.
old-location: fax\_mfax_faxrecipients_add_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_73l0.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],FaxRecipients object, FaxRecipients object [Fax Service],Add method, FaxRecipients.Add, IFaxRecipients.Add, IFaxRecipients::Add, _mfax_faxrecipients.add, fax._mfax_faxrecipients_add, fax._mfax_faxrecipients_add_vb
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
 - FaxRecipients.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRecipients::Add


## -description


The <b>Add</b> method adds a new <a href="https://msdn.microsoft.com/library/ms690204(v=VS.85).aspx">FaxRecipient</a> object to the <a href="https://msdn.microsoft.com/library/ms689604(v=VS.85).aspx">FaxRecipients</a> collection. 


## -parameters




### -param bstrFaxNumber

Type: <b>String</b>

Specifies the fax number of the fax recipient.


### -param bstrRecipientName [optional]

Type: <b>String</b>

Specifies the name of the fax recipient. 


### -param ppFaxRecipient






## -returns



Type: <b><a href="https://msdn.microsoft.com/library/ms690206(v=VS.85).aspx">IFaxRecipient</a>**</b>

A <a href="https://msdn.microsoft.com/library/ms690204(v=VS.85).aspx">FaxRecipient</a> object.




## -see-also




<a href="https://msdn.microsoft.com/library/ms693479(v=VS.85).aspx">Broadcasting a Fax</a>



<a href="https://msdn.microsoft.com/library/ms689604(v=VS.85).aspx">FaxRecipients</a>



<a href="https://msdn.microsoft.com/library/ms689605(v=VS.85).aspx">IFaxRecipients</a>
 

 

