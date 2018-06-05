---
UID: NF:ole2.OleCreateLinkFromData
title: OleCreateLinkFromData function
author: windows-sdk-content
description: Creates a linked object from a data transfer object retrieved either from the clipboard or as part of an OLE drag-and-drop operation.
old-location: com\olecreatelinkfromdata.htm
old-project: com
ms.assetid: 3eda0cf5-c33d-43cf-ba8a-02a4f6383adc
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: OleCreateLinkFromData, OleCreateLinkFromData function [COM], _ole_OleCreateLinkFromData, com.olecreatelinkfromdata, ole2/OleCreateLinkFromData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole2.h
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
tech.root: 
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
api_name:
-	OleCreateLinkFromData
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OleCreateLinkFromData function


## -description


Creates a linked object from a data transfer object retrieved either from the clipboard or as part of an OLE drag-and-drop operation.




## -parameters




### -param pSrcDataObj [in]

Pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data transfer object from which the linked object is to be created.


### -param riid [in]

Reference to the identifier of interface the caller later uses to communicate with the new object (usually IID_IOleObject, defined in the OLE headers as the interface identifier for <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>).


### -param renderopt [in]

Value from the enumeration <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. Additional considerations are described in the following Remarks section.


### -param pFormatEtc [in]

 Pointer to a value from the enumeration <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. The <b>OLERENDER</b> value chosen affects the possible values for the <i>pFormatEtc</i> parameter.


### -param pClientSite [in]

 Pointer to an instance of <a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a>, the primary interface through which the object will request services from its container. This parameter can be <b>NULL</b>.


### -param pStg [in]

Pointer to the <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the storage object. This parameter cannot be <b>NULL</b>.


### -param ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return,   <i>ppvObj</i> contains the requested interface pointer on the newly created object.


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
Not able to open the clipboard.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_CANT_GETMONIKER</b></dt>
</dl>
</td>
<td width="60%">
Not able to extract the object's moniker.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_CANT_BINDTOSOURCE</b></dt>
</dl>
</td>
<td width="60%">
Not able to bind to source. Binding is necessary to get the cache's initialization data.


</td>
</tr>
</table>
 




## -remarks



The <b>OleCreateLinkFromData</b> function is used to implement either a paste-link or a drag-link operation. Its operation is similar to that of the <a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a> function, except that it creates a link, and looks for different data formats. If the CF_LINKSOURCE format is not present, and either the FileName or FileNameW clipboard format is present in the data transfer object, <b>OleCreateLinkFromData</b> creates a package containing the link to the indicated file.



You use the renderopt and <i>pFormatetc</i> parameters to control the caching capability of the newly created object. For general information on how to determine what is to be cached, refer to the <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a> enumeration for a description of the interaction between renderopt and <i>pFormatetc</i>. There are, however, some additional specific effects of these parameters on the way <b>OleCreateLinkFromData</b> initializes the cache, as follows.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>
OLERENDER_DRAW, OLERENDER_FORMAT


</td>
<td>
If the presentation information is in the other formats in the source data object, this information is used. If the information is not present, the cache is initially empty, but will be filled the first time the object is run. No other formats are cached in the newly created object.


</td>
</tr>
<tr>
<td>
OLERENDER_NONE, OLERENDER_ASIS


</td>
<td>
Nothing is to be cached in the newly created object.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ef52dc37-aa63-47f3-a04f-f9d22178690f">OleCreateLink</a>
 

 

