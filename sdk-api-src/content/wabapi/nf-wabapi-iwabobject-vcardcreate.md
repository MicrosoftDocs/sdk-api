---
UID: NF:wabapi.IWABObject.VCardCreate
title: IWABObject::VCardCreate
author: windows-sdk-content
description: Translates the properties of a given MailUser object into a vCard file.
old-location: wab\_wab_IWABObject_VCardCreate.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\vcardcreate.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWABObject interface [Windows Address Book],VCardCreate method, IWABObject.VCardCreate, IWABObject::VCardCreate, VCardCreate, VCardCreate method [Windows Address Book], VCardCreate method [Windows Address Book],IWABObject interface, _wab_IWABObject_VCardCreate, wab._wab_IWABObject_VCardCreate, wabapi/IWABObject::VCardCreate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wabapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Wab32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IWABObject.VCardCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IWABObject::VCardCreate


## -description


Translates the properties of a given MailUser object into a 
		vCard file.


## -parameters




### -param lpIAB

Type: <b><a href="https://msdn.microsoft.com/df614598-b9ac-462a-89e7-cda0a602c6cd">IAddrBook</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/df614598-b9ac-462a-89e7-cda0a602c6cd">IAddrBook</a>interface that 
				specifies the address book.


### -param ulFlags

Type: <b>ULONG</b>

No flags.


### -param lpszVCard

Type: <b>LPSTR</b>

Value of type <b>LPSTR</b> that specifies the 
				string containing the complete path name of the file to create.
				


### -param lpMailUser

Type: <b><a href="https://msdn.microsoft.com/7af094d9-b5fd-4214-9604-b7dd93639f5e">IMailUser</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/7af094d9-b5fd-4214-9604-b7dd93639f5e">IMailUser</a> interface that 
				specifies the object whose properties are to be written into 
				the file.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The complete file name must be specified. If the file already exists, 
	it will be overwritten. Vcard creation is extensible: if your client 
	application is using named properties to store client-specific data in the 
	Windows Address Book (WAB), it may be possible to include this data in the newly 
	created vCard.




## -see-also




<a href="https://msdn.microsoft.com/cba6a6ae-79e5-4412-9e1e-ad0ef41b1862">IWABObject</a>



<a href="https://msdn.microsoft.com/40638b23-e956-4fe8-b132-245c43df6890">Importing and Exporting Named Properties Through vCards</a>
 

 

