---
UID: NF:ole2.OleGetClipboardWithEnterpriseInfo
title: OleGetClipboardWithEnterpriseInfo function (ole2.h)
description: Enables Windows Information Protection enlightened applications to retrieve an IDataObject from the OLE Clipboard accompanied by Windows Information Protection information about the data and the source application.
helpviewer_keywords: ["OleGetClipboardWithEnterpriseInfo","OleGetClipboardWithEnterpriseInfo function [COM]","com.olegetclipboardwithenterpriseinfo","ole2/OleGetClipboardWithEnterpriseInfo"]
old-location: com\olegetclipboardwithenterpriseinfo.htm
tech.root: com
ms.assetid: 1DAD2A9A-EDA2-49D2-90F7-2A9022988177
ms.date: 12/05/2018
ms.keywords: OleGetClipboardWithEnterpriseInfo, OleGetClipboardWithEnterpriseInfo function [COM], com.olegetclipboardwithenterpriseinfo, ole2/OleGetClipboardWithEnterpriseInfo
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleGetClipboardWithEnterpriseInfo
 - ole2/OleGetClipboardWithEnterpriseInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-RTCore-OLE32-clipboard-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-ole32-clipboard-ie-l1-1-0.dll
 - API-MS-Win-RTCore-Ole32-Clipboard-L1-1-1.dll
api_name:
 - OleGetClipboardWithEnterpriseInfo
---

# OleGetClipboardWithEnterpriseInfo function


## -description

Enables Windows Information Protection enlightened  
applications to retrieve an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> from the OLE Clipboard  
accompanied by Windows Information Protection information about the data and the  
source application.This information allows the  
enlightened application to take over responsibility for applying Windows Information Protection  
policy, including flying any appropriate UI prompts, and  
auditing cases where the user explicitly approves copying  
enterprise data into a personal context.  


If the calling application is not enlightened, or is  
configured as "unallowed" to access enterprise data,  
then this call behaves exactly like <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleGetClipboard</a> - applying policy before deciding what <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> to return,  
and supplying empty strings as output.

## -parameters

### -param dataObject [out]

Address of <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> pointer variable that receives the interface pointer to the clipboard data object.

### -param dataEnterpriseId [out]

The enterprise id of the application that set the clipboard data. 
If the data is personal, this will be an empty string.

### -param sourceDescription [out]

 The description of the application that set the clipboard.

### -param targetDescription [out]

The         description of the caller's application to be used in auditing.

### -param dataDescription [out]

The description of the data object to be used in auditing.

## -returns

This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CLIPBRD_E_CANT_OPEN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/winuser/nf-winuser-openclipboard">OpenClipboard</a> function used within <a href="/windows/desktop/api/ole2/nf-ole2-oleflushclipboard">OleFlushClipboard</a> failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CLIPBRD_E_CANT_CLOSE</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/winuser/nf-winuser-closeclipboard">CloseClipboard</a> function used within <a href="/windows/desktop/api/ole2/nf-ole2-oleflushclipboard">OleFlushClipboard</a> failed.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Caution</b>  Clipboard data is not trusted. Parse the data carefully before using it in your application.</div>
<div> </div>
If you are writing an application that can accept data from the clipboard, call the <b>OleGetClipboardWithEnterpriseInfo</b> function to get a pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface that you can use to retrieve the contents of the clipboard.

<b>OleGetClipboardWithEnterpriseInfo</b> handles three cases: 



<ul>
<li>The application that placed data on the clipboard with the <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a> function is still running.</li>
<li>The application that placed data on the clipboard with the <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a> function has subsequently called the <a href="/windows/desktop/api/ole2/nf-ole2-oleflushclipboard">OleFlushClipboard</a> function.</li>
<li>There is data from a non-OLE application on the clipboard.</li>
</ul>
In the first case, the clipboard data object returned by <b>OleGetClipboardWithEnterpriseInfo</b> may forward calls as necessary to the original data object placed on the clipboard and, thus, can potentially make RPC calls.

In the second case, OLE creates a default data object and returns it to the user. Because the data on the clipboard originated from an <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a> call, the OLE-provided data object contains more accurate information about the type of data on the clipboard. In particular, the original medium (TYMED) on which the data was offered is known. Thus, if a data-source application offers a particular clipboard format, for example cfFOO, on a storage object and calls the <a href="/windows/desktop/api/ole2/nf-ole2-oleflushclipboard">OleFlushClipboard</a> function, the storage object is copied into memory and the hglobal memory handle is put on the clipboard. Then, when the <b>OleGetClipboardWithEnterpriseInfo</b> function creates its default data object, the hglobal from the clipboard again becomes an <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> object. Furthermore, the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> enumerator and the <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-querygetdata">IDataObject::QueryGetData</a> method would all correctly indicate that the original clipboard format (cfFOO) is again available on a TYMED_ISTORAGE.

In the third case, OLE still creates a default data object, but there is no special information about the data in the clipboard formats (particularly for application-defined Clipboard formats). Thus, if an hGlobal-based storage medium were put on the clipboard directly by a call to the <a href="/windows/desktop/api/winuser/nf-winuser-setclipboarddata">SetClipboardData</a> function, the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> enumerator and the <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-querygetdata">IDataObject::QueryGetData</a> method would not indicate that the data was available on a storage medium. A call to the <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> method for TYMED_ISTORAGE would succeed, however. Because of these limitations, it is strongly recommended that OLE-aware applications interact with the clipboard using the OLE clipboard functions.



The clipboard data object created by the <b>OleGetClipboardWithEnterpriseInfo</b> function has a fairly extensive <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> implementation. The OLE-provided data object can convert OLE 1 clipboard format data into the representation expected by an OLE 2 caller. Also, any structured data is available on any structured or flat medium, and any flat data is available on any flat medium. However, GDI objects (such as metafiles and bitmaps) are only available on their respective mediums.



Note that the tymed member of the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure used in the <b>FORMATETC</b> enumerator contains the union of supported mediums. Applications looking for specific information (such as whether CF_TEXT is available on TYMED_HGLOBAL) should do the appropriate bitmasking when checking this value.



If you call the <b>OleGetClipboardWithEnterpriseInfo</b> function, you should only hold on to the returned <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> for a very short time. It consumes resources in the application that offered it.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleGetClipboard</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a>