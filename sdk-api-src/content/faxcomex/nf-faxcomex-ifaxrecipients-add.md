---
UID: NF:faxcomex.IFaxRecipients.Add
title: IFaxRecipients::Add
author: windows-driver-content
description: The Add method adds a new FaxRecipient object to the FaxRecipients collection.
old-location: fax\_mfax_faxrecipients_add_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_73l0.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],FaxRecipients object, FaxRecipients object [Fax Service],Add method, FaxRecipients.Add, IFaxRecipients.Add, IFaxRecipients::Add, _mfax_faxrecipients.add, fax._mfax_faxrecipients_add, fax._mfax_faxrecipients_add_vb
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
-	FaxRecipients.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRecipients::Add


## -description


The <b>Add</b> method adds a new <a href="https://msdn.microsoft.com/e418dbaf-9b07-40a9-bab8-7b4561b63325">FaxRecipient</a> object to the <a href="https://msdn.microsoft.com/b0210d82-5d62-4192-a05c-455c9f3adf9b">FaxRecipients</a> collection. 


## -parameters




### -param bstrFaxNumber

Type: <b>String</b>

Specifies the fax number of the fax recipient.


### -param bstrRecipientName [optional]

Type: <b>String</b>

Specifies the name of the fax recipient. 


### -param ppFaxRecipient






## -returns



Type: <b><a href="https://msdn.microsoft.com/2c8073de-644e-4594-8e52-49d07e82d432">IFaxRecipient</a>**</b>

A <a href="https://msdn.microsoft.com/e418dbaf-9b07-40a9-bab8-7b4561b63325">FaxRecipient</a> object.




## -see-also




<a href="https://msdn.microsoft.com/82a9e599-35d3-4fca-954f-dbc579c023f5">Broadcasting a Fax</a>



<a href="https://msdn.microsoft.com/b0210d82-5d62-4192-a05c-455c9f3adf9b">FaxRecipients</a>



<a href="https://msdn.microsoft.com/b2481702-3e83-4b99-87ba-d9af9fdd63aa">IFaxRecipients</a>
 

 

