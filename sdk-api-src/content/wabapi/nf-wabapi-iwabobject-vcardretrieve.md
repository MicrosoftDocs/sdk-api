---
UID: NF:wabapi.IWABObject.VCardRetrieve
title: IWABObject::VCardRetrieve (wabapi.h)
description: Reads a vCard file and creates a MailUser object containing the vCard properties.
helpviewer_keywords: ["IWABObject interface [Windows Address Book]","VCardRetrieve method","IWABObject.VCardRetrieve","IWABObject::VCardRetrieve","VCardRetrieve","VCardRetrieve method [Windows Address Book]","VCardRetrieve method [Windows Address Book]","IWABObject interface","WAB_VCARD_FILE","WAB_VCARD_STREAM","_wab_IWABObject_VCardRetrieve","wab._wab_IWABObject_VCardRetrieve","wabapi/IWABObject::VCardRetrieve"]
old-location: wab\_wab_IWABObject_VCardRetrieve.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\vcardretrieve.htm
ms.date: 12/05/2018
ms.keywords: IWABObject interface [Windows Address Book],VCardRetrieve method, IWABObject.VCardRetrieve, IWABObject::VCardRetrieve, VCardRetrieve, VCardRetrieve method [Windows Address Book], VCardRetrieve method [Windows Address Book],IWABObject interface, WAB_VCARD_FILE, WAB_VCARD_STREAM, _wab_IWABObject_VCardRetrieve, wab._wab_IWABObject_VCardRetrieve, wabapi/IWABObject::VCardRetrieve
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
 - IWABObject::VCardRetrieve
 - wabapi/IWABObject::VCardRetrieve
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
 - IWABObject.VCardRetrieve
---

# IWABObject::VCardRetrieve


## -description

Reads a vCard file and creates a MailUser object containing 
		the vCard properties.

## -parameters

### -param lpIAB

Type: <b><a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a>*</b>

Pointer to an <a href="/windows/desktop/api/wabiab/nn-wabiab-iaddrbook">IAddrBook</a> interface 
				that specifies the address book object.

### -param ulFlags

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies flags 
				affecting behavior.



#### WAB_VCARD_FILE

Indicates that the <i>lpszVCard</i> parameter is 
				the path name of the file to be read.



#### WAB_VCARD_STREAM

Indicates that the <i>lpszVCard</i> parameter 
		points to a buffer that contains the full contents of the Vcard.

### -param lpszVCard

Type: <b>LPSTR</b>

Pointer to a string containing either the complete path name of the 
				file to be read or the vCard buffer.

### -param lppMailUser

Type: <b><a href="/windows/desktop/api/wabdefs/nn-wabdefs-imailuser">IMailUser</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/wabdefs/nn-wabdefs-imailuser">IMailUser</a> interface that 
				receives the MailUser object created containing the properties 
				in the vCard file.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Vcard retrieval is extensible. If your client application is using 
	named properties to store client-specific data in the Windows Address Book (WAB) 
	and exporting them to vCards, it is possible to extend the 
	WAB vCard engine to read this data from a vCard. 
	For more information, see <a href="https://msdn.microsoft.com/40638b23-e956-4fe8-b132-245c43df6890">Importing and 
	Exporting Named Properties Through vCards</a>. The <i>lpszVCard</i> 
	parameter can be a pointer to a Vcard file name or a pointer to a <b>NULL</b>-terminated string containing the full contents of the Vcard. To have the pointer indicate which content it represents, set the <i>ulFlags</i> parameter to either 
<b>WAB_VCARD_FILE</b> or 
<b>WAB_VCARD_STREAM</b>. The former setting indicates a 
file name, and the latter setting indicates a pointer to a buffer with the 
Vcard contents.