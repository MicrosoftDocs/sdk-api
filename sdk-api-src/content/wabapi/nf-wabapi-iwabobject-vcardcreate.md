---
UID: NF:wabapi.IWABObject.VCardCreate
title: IWABObject::VCardCreate (wabapi.h)
author: windows-sdk-content
description: Translates the properties of a given MailUser object into a vCard file.
old-location: wab\_wab_IWABObject_VCardCreate.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\vcardcreate.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWABObject interface [Windows Address Book],VCardCreate method, IWABObject.VCardCreate, IWABObject::VCardCreate, VCardCreate, VCardCreate method [Windows Address Book], VCardCreate method [Windows Address Book],IWABObject interface, _wab_IWABObject_VCardCreate, wab._wab_IWABObject_VCardCreate, wabapi/IWABObject::VCardCreate
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
ms.custom: 19H1
---

# IWABObject::VCardCreate


## -description


Translates the properties of a given MailUser object into a 
		vCard file.


## -parameters




### -param lpIAB

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms629649(v=VS.85).aspx">IAddrBook</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms629649(v=VS.85).aspx">IAddrBook</a>interface that 
				specifies the address book.


### -param ulFlags

Type: <b>ULONG</b>

No flags.


### -param lpszVCard

Type: <b>LPSTR</b>

Value of type <b>LPSTR</b> that specifies the 
				string containing the complete path name of the file to create.
				


### -param lpMailUser

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms629507(v=VS.85).aspx">IMailUser</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms629507(v=VS.85).aspx">IMailUser</a> interface that 
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




<a href="https://msdn.microsoft.com/en-us/library/ms629467(v=VS.85).aspx">IWABObject</a>



<a href="https://msdn.microsoft.com/en-us/library/ms629732(v=VS.85).aspx">Importing and Exporting Named Properties Through vCards</a>
 

 

