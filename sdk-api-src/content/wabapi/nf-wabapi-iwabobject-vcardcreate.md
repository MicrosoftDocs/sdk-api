---
UID: NF:wabapi.IWABObject.VCardCreate
title: IWABObject::VCardCreate (wabapi.h)
description: Translates the properties of a given MailUser object into a vCard file.
helpviewer_keywords: ["IWABObject interface [Windows Address Book]","VCardCreate method","IWABObject.VCardCreate","IWABObject::VCardCreate","VCardCreate","VCardCreate method [Windows Address Book]","VCardCreate method [Windows Address Book]","IWABObject interface","_wab_IWABObject_VCardCreate","wab._wab_IWABObject_VCardCreate","wabapi/IWABObject::VCardCreate"]
old-location: wab\_wab_IWABObject_VCardCreate.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\vcardcreate.htm
ms.date: 12/05/2018
ms.keywords: IWABObject interface [Windows Address Book],VCardCreate method, IWABObject.VCardCreate, IWABObject::VCardCreate, VCardCreate, VCardCreate method [Windows Address Book], VCardCreate method [Windows Address Book],IWABObject interface, _wab_IWABObject_VCardCreate, wab._wab_IWABObject_VCardCreate, wabapi/IWABObject::VCardCreate
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IWABObject::VCardCreate
 - wabapi/IWABObject::VCardCreate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IWABObject.VCardCreate
---

# IWABObject::VCardCreate


## -description

Translates the properties of a given MailUser object into a 
		vCard file.

## -parameters

### -param lpIAB

Type: <b><a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a>*</b>

Pointer to an <a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a> interface that 
				specifies the address book.

### -param ulFlags

Type: <b>ULONG</b>

No flags.

### -param lpszVCard

Type: <b>LPSTR</b>

Value of type <b>LPSTR</b> that specifies the 
				string containing the complete path name of the file to create.

### -param lpMailUser

Type: <b><a href="/windows/desktop/api/wabdefs/nn-wabdefs-imailuser">IMailUser</a>*</b>

Pointer to an <a href="/windows/desktop/api/wabdefs/nn-wabdefs-imailuser">IMailUser</a> interface that 
				specifies the object whose properties are to be written into 
				the file.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The complete file name must be specified. If the file already exists, 
	it will be overwritten. Vcard creation is extensible: if your client 
	application is using named properties to store client-specific data in the 
	Windows Address Book (WAB), it may be possible to include this data in the newly 
	created vCard.

## -see-also

<a href="/windows/desktop/api/wabapi/nn-wabapi-iwabobject">IWABObject</a>



<a href="/previous-versions/windows/desktop/wab/-wab-vcardprops">Importing and Exporting Named Properties Through vCards</a>