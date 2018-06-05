---
UID: NF:ole2.OleCreateFromData
title: OleCreateFromData function
author: windows-sdk-content
description: Creates an embedded object from a data transfer object retrieved either from the clipboard or as part of an OLE drag-and-drop operation. It is intended to be used to implement a paste from an OLE drag-and-drop operation.
old-location: com\olecreatefromdata.htm
old-project: com
ms.assetid: aa5e997e-60d4-472d-9c81-5359c277bde3
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: OleCreateFromData, OleCreateFromData function [COM], _ole_OleCreateFromData, com.olecreatefromdata, ole2/OleCreateFromData
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
-	ext-ms-win-com-ole32-l1-1-3.dll
-	Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
-	OleCreateFromData
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OleCreateFromData function


## -description


Creates an embedded object from a data transfer object retrieved either from the clipboard or as part of an OLE drag-and-drop operation. It is intended to be used to implement a paste from an OLE drag-and-drop operation.




## -parameters




### -param pSrcDataObj [in]

Pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data transfer object that holds the data from which the object is created.


### -param riid [in]

Reference to the identifier of the interface the caller later uses to communicate with the new object (usually IID_IOleObject, defined in the OLE headers as the interface identifier for <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>).


### -param renderopt [in]

Value from the enumeration <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. Additional considerations are described in the following Remarks section.


### -param pFormatEtc [in]

 Pointer to a value from the enumeration <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. The <b>OLERENDER</b> value chosen affects the possible values for the <i>pFormatEtc</i> parameter.


### -param pClientSite [in]

Pointer to an instance of <a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a>, the primary interface through which the object will request services from its container. This parameter can be <b>NULL</b>.


### -param pStg [in]

Pointer to the <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the storage object. This parameter may not be <b>NULL</b>.


### -param ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly created object.


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
<dt><b>OLE_E_STATIC</b></dt>
</dl>
</td>
<td width="60%">
Indicates OLE can create only a static object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_FORMATETC</b></dt>
</dl>
</td>
<td width="60%">
No acceptable formats are available for object creation.

</td>
</tr>
</table>
 




## -remarks



The <b>OleCreateFromData</b> function creates an embedded object from a data transfer object supporting the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface. The data object in this case is either the type retrieved from the clipboard with a call to the <a href="https://msdn.microsoft.com/c5e7badb-339b-48d5-8c9a-3950e2ffe6bf">OleGetClipboard</a> function or is part of an OLE drag-and-drop operation (the data object is passed to a call to <a href="https://msdn.microsoft.com/7ea6d815-bf8f-47d5-99d3-f9a55bafee2e">IDropTarget::Drop</a>).

If either the FileName or FileNameW clipboard format (CF_FILENAME) is present in the data transfer object, and CF_EMBEDDEDOBJECT or CF_EMBEDSOURCE do not exist, <b>OleCreateFromData</b> first attempts to create a package containing the indicated file. Generally, it takes the first available format. 

If <b>OleCreateFromData</b> cannot create a package, it tries to create an object using the CF_EMBEDDEDOBJECT format. If that format is not available, <b>OleCreateFromData</b> tries to create it with the CF_EMBEDSOURCE format. If neither of these formats is available and the data transfer object supports the <a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a> interface, <b>OleCreateFromData</b> calls the object's <a href="https://msdn.microsoft.com/3a200812-48d9-4202-987a-1400aa66191c">IPersistStorage::Save</a> to have the object save itself.



If an existing linked object is selected, then copied, it appears on the clipboard as just another embeddable object. Consequently, a paste operation that invokes <b>OleCreateFromData</b> may create a linked object. After the paste operation, the container should call the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> function, requesting IID_IOleLink (defined in the OLE headers as the interface identifier for <a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a>), to determine if a linked object was created.



Use the <i>renderopt</i> and <i>pFormatetc</i> parameters to control the caching capability of the newly created object. For general information about using the interaction of these parameters to determine what is to be cached, refer to the <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a> enumeration. There are, however, some additional specific effects of these parameters on the way <b>OleCreateFromData</b> initializes the cache.



When <b>OleCreateFromData</b> uses either the CF_EMBEDDEDOBJECT or the CF_EMBEDSOURCE clipboard format to create the embedded object, the main difference between the two is where the cache-initialization data is stored: 



<ul>
<li>CF_EMBEDDEDOBJECT indicates that the source is an existing embedded object. It already has in its cache the appropriate data, and OLE uses this data to initialize the cache of the new object. 
</li>
<li>CF_EMBEDSOURCE indicates that the source data object contains the cache-initialization information in formats other than CF_EMBEDSOURCE. <b>OleCreateFromData</b> uses these to initialize the cache of the newly embedded object. </li>
</ul>
The <i>renderopt</i> values affect cache initialization as follows.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>
OLERENDER_DRAW &amp; OLERENDER_FORMAT


</td>
<td>
If the presentation information to be cached is currently present in the appropriate cache-initialization pool, it is used. (Appropriate locations are in the source data object cache for CF_EMBEDDEDOBJECT, and in the other formats in the source data object for CF_EMBEDSOURCE.) If the information is not present, the cache is initially empty, but will be filled the first time the object is run. No other formats are cached in the newly created object.


</td>
</tr>
<tr>
<td>
OLERENDER_NONE


</td>
<td>
Nothing is to be cached in the newly created object. If the source has the CF_EMBEDDEDOBJECT format, any existing cached data that has been copied is removed.


</td>
</tr>
<tr>
<td>
OLERENDER_ASIS


</td>
<td>
If the source has the CF_EMBEDDEDOBJECT format, the cache of the new object is to contain the same cache data as the source object. For CF_EMBEDSOURCE, nothing is to be cached in the newly created object. This option should be used by more sophisticated containers. After this call, such containers would call <a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a> and <a href="https://msdn.microsoft.com/a6a57bdd-190f-485b-9b46-cbfc1a1d29a6">IOleCache::Uncache</a> to set up exactly what is to be cached. For CF_EMBEDSOURCE, they would then also call <a href="https://msdn.microsoft.com/4b1f2fb6-636c-47dd-8f89-884f7b4f3977">IOleCache::InitCache</a>.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>



<a href="https://msdn.microsoft.com/00b7edd2-8e2e-4e0a-91a6-d966f6c8d456">OleCreate</a>
 

 

