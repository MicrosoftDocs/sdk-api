---
UID: NF:msinkaut.IInkDisp.Save
title: IInkDisp::Save (msinkaut.h)
description: Converts the ink to the specified InkPersistenceFormat, saves the ink by using the specified InkPersistenceCompressionMode, and returns the binary data in an array of bytes.
helpviewer_keywords: ["31da19a7-207f-4f11-9b0f-7402e9727f59","Base64Gif","Base64InkSerializedFormat","Gif","IInkDisp interface [Tablet PC]","Save method","IInkDisp.Save","IInkDisp::Save","IPCM_Default","IPCM_MaximumCompression","IPCM_NoCompression","InkSerializedFormat","Save","Save method [Tablet PC]","Save method [Tablet PC]","IInkDisp interface","msinkaut/IInkDisp::Save","tablet.inkdisp_save"]
old-location: tablet\inkdisp_save.htm
tech.root: tablet
ms.assetid: 31da19a7-207f-4f11-9b0f-7402e9727f59
ms.date: 12/05/2018
ms.keywords: 31da19a7-207f-4f11-9b0f-7402e9727f59, Base64Gif, Base64InkSerializedFormat, Gif, IInkDisp interface [Tablet PC],Save method, IInkDisp.Save, IInkDisp::Save, IPCM_Default, IPCM_MaximumCompression, IPCM_NoCompression, InkSerializedFormat, Save, Save method [Tablet PC], Save method [Tablet PC],IInkDisp interface, msinkaut/IInkDisp::Save, tablet.inkdisp_save
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkDisp::Save
 - msinkaut/IInkDisp::Save
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkDisp.Save
---

# IInkDisp::Save


## -description

Converts the ink to the specified <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat">InkPersistenceFormat</a>, saves the ink by using the specified <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistencecompressionmode">InkPersistenceCompressionMode</a>, and returns the binary data in an array of bytes.

## -parameters

### -param PersistenceFormat [in, optional]

Optional. Sets one of the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat">InkPersistenceFormat</a> values that indicates the format of the persisted ink. The default value is InkSerializedFormat.
            

<table>
<tr>
<th>Name
              </th>
<th>Description
              </th>
</tr>
<tr>
<td width="40%"><a id="InkSerializedFormat"></a><a id="inkserializedformat"></a><a id="INKSERIALIZEDFORMAT"></a><dl>
<dt><b>InkSerializedFormat</b></dt>
</dl>
</td>
<td width="60%">
Ink is persisted using ink serialized format (ISF).
                

This is the most compact persistent representation of ink. It can be embedded within a binary document format or placed directly on the Clipboard. This is the default value.

</td>
</tr>
<tr>
<td width="40%"><a id="Base64InkSerializedFormat"></a><a id="base64inkserializedformat"></a><a id="BASE64INKSERIALIZEDFORMAT"></a><dl>
<dt><b>Base64InkSerializedFormat</b></dt>
</dl>
</td>
<td width="60%">
Ink is persisted by encoding the ISF as a base64 stream.

This format is provided so that ink can be encoded directly in an Extensible Markup Language (XML) or HTML file.

</td>
</tr>
<tr>
<td width="40%"><a id="Gif"></a><a id="gif"></a><a id="GIF"></a><dl>
<dt><b>Gif</b></dt>
</dl>
</td>
<td width="60%">
Ink is persisted by using a Graphics Interchange Format (GIF) file that contains ISF as metadata that is embedded within the file. 

This allows ink to be viewed in applications that are not ink-enabled and maintain its full ink fidelity when it returns to an ink-enabled application. This format is ideal when transporting ink content within an HTML file and making it usable by ink-enabled and ink-unaware applications.
                

</td>
</tr>
<tr>
<td width="40%"><a id="Base64Gif"></a><a id="base64gif"></a><a id="BASE64GIF"></a><dl>
<dt><b>Base64Gif</b></dt>
</dl>
</td>
<td width="60%">
Ink is persisted by using a base64 encoded fortified. 

This GIFformat is provided when ink is to be encoded directly in an XML or HTML file with later conversion into an image. A possible use of this would be in an XML format that is generated to contain all ink information and used as a way to generate HTML through Extensible Stylesheet Language Transformations (XSLT).

</td>
</tr>
</table>

### -param CompressionMode [in, optional]

Optional. One of the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistencecompressionmode">InkPersistenceCompressionMode</a> values that specifies the compression mode of the persisted ink.
            The default value is IPCM_Default.

<table>
<tr>
<th>Name
              </th>
<th>Description
              </th>
</tr>
<tr>
<td width="40%"><a id="IPCM_Default"></a><a id="ipcm_default"></a><a id="IPCM_DEFAULT"></a><dl>
<dt><b>IPCM_Default</b></dt>
</dl>
</td>
<td width="60%">
Is used when  the best tradeoff between save-time and storage for the typical application is needed.

</td>
</tr>
<tr>
<td width="40%"><a id="IPCM_MaximumCompression"></a><a id="ipcm_maximumcompression"></a><a id="IPCM_MAXIMUMCOMPRESSION"></a><dl>
<dt><b>IPCM_MaximumCompression</b></dt>
</dl>
</td>
<td width="60%">
Is used when minimizing storage space is more important than how fast the ink is saved.

</td>
</tr>
<tr>
<td width="40%"><a id="IPCM_NoCompression"></a><a id="ipcm_nocompression"></a><a id="IPCM_NOCOMPRESSION"></a><dl>
<dt><b>IPCM_NoCompression</b></dt>
</dl>
</td>
<td width="60%">
Is used when save-time is more important than the amount of storage space used and when compatibility between versions is important.

</td>
</tr>
</table>

### -param Data [out, retval]

When this method returns, contains the byte array that contains the persisted ink.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid compression mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate byte array.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Occurs if you attempt to save an empty Ink object in GIF format.

</td>
</tr>
</table>

## -remarks

Attempting to save an empty <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object in GIF format generates an error.
          

<div class="alert"><b>Note</b>  When calling the <b>Save</b> method with an <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat">InkPersistenceFormat</a> value of <b>Base64InkSerializedFormat</b>, the return value is a <b>NULL</b> -terminated byte array. To write the saved ink to an XML file, first remove the last byte from the array before converting the array to 8-bit Unicode Transformation Format (UTF-8) encoded string.
          </div>
<div> </div>

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistencecompressionmode">InkPersistenceCompressionMode Enumeration</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat">InkPersistenceFormat Enumeration</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load">Load Method</a>
