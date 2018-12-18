---
UID: NE:fxsutility.__unnamed_enum_0
title: SendToMode
author: windows-sdk-content
description: Defines the way a file will be faxed from within an application. With Windows Vista there is only one possible value.
old-location: fax\_mfax_sendtomode.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\shellextension\e\faxinto_z_sendtomode.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SEND_TO_FAX_RECIPIENT_ATTACHMENT, SendToMode, SendToMode enumeration [Fax Service], _mfax_sendtomode, fax._mfax_sendtomode, fxsutility/SEND_TO_FAX_RECIPIENT_ATTACHMENT, fxsutility/SendToMode
ms.topic: enum
req.header: fxsutility.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - HeaderDef
api_location:
 - Fxsutility.h
api_name:
 - SendToMode
product: Windows
targetos: Windows
req.typenames: SendToMode
req.redist: 
---

# SendToMode enumeration


## -description


Defines the way a file will be faxed from within an application. With Windows Vista there is only one possible value.


## -enum-fields




### -field SEND_TO_FAX_RECIPIENT_ATTACHMENT

The file is faxed as it is. The user cannot add typed material preceding it or following it.


## -remarks



This enumeration is used primarily as a parameter for the <a href="https://msdn.microsoft.com/19ab50a4-a2fb-40be-a9e8-e29d149bb274">SendToFaxRecipient</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/19ab50a4-a2fb-40be-a9e8-e29d149bb274">SendToFaxRecipient</a>



<a href="https://msdn.microsoft.com/555ee494-ee1c-4047-b7ae-a890176a6b32">Shell Fax Extension Functions</a>
 

 

