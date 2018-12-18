---
UID: NF:ole2.OleConvertOLESTREAMToIStorage
title: OleConvertOLESTREAMToIStorage function
author: windows-sdk-content
description: Converts the specified object from the OLE 1 storage model to an OLE 2 structured storage object without specifying presentation data.
old-location: stg\oleconvertolestreamtoistorage.htm
tech.root: stg
ms.assetid: 8fed879c-5f97-4450-8259-da9643dd828c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OleConvertOLESTREAMToIStorage, OleConvertOLESTREAMToIStorage function [Structured Storage], _stg_oleconvertolestreamtoistorage, ole2/OleConvertOLESTREAMToIStorage, stg.oleconvertolestreamtoistorage
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleConvertOLESTREAMToIStorage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OleConvertOLESTREAMToIStorage function


## -description


The 
<b>OleConvertOLESTREAMToIStorage</b> function converts the specified object from the OLE 1 storage model to an OLE 2 structured storage object without specifying presentation data.
<div class="alert"><b>Note</b>  This is one of several compatibility functions.</div><div> </div>

## -parameters




### -param lpolestream [in]

A pointer to a stream that contains the persistent representation of the object in the OLE 1 storage format.


### -param pstg [out]

A pointer to the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the OLE 2 structured storage object.


### -param ptd [in]

A pointer to the 
<a href="https://msdn.microsoft.com/en-us/library/ms686613(v=VS.85).aspx">DVTARGETDEVICE</a> structure that specifies the target device for which the OLE 1 object is rendered.


## -returns



This function supports the standard return value <b>E_INVALIDARG</b>, in addition to the following:




## -remarks



This function converts an OLE 1 object to an OLE 2 structured storage object. Use this function to update OLE 1 objects to OLE 2 objects when a new version of the object application supports OLE 2.

On entry, the <i>lpolestm</i> parameter should be created and positioned just as it would be for an 
<a href="https://msdn.microsoft.com/en-us/library/ms680103(v=VS.85).aspx">OleLoadFromStream</a> function call. On exit, the <i>lpolestm</i> parameter is positioned just as it would be on exit from an <b>OleLoadFromStream</b> function, and the <i>pstg</i> parameter contains the uncommitted persistent representation of the OLE 2 storage object.

For OLE 1 objects that use native data for their presentation, the 
<b>OleConvertOLESTREAMToIStorage</b> function returns <b>CONVERT10_S_NO_PRESENTATION</b>. On receiving this return value, callers should call <a href="https://msdn.microsoft.com/library/ms679699(v=VS.85).aspx">IOleObject::Update</a> to get the presentation data so it can be written to storage.

Applications that do not use the OLE default caching resources, but use the conversion resources, can use an alternate function, 
<a href="https://msdn.microsoft.com/2e77fa0e-1d98-4c59-8d3c-65bd7235ec8f">OleConvertOLESTREAMToIStorageEx</a>, which can specify the presentation data to convert. In the 
<b>OleConvertOLESTREAMToIStorageEx</b> function, the presentation data read from the <b>OLESTREAM</b> structure is passed out and the newly created OLE 2 storage object does not contain a presentation stream.

The following procedure describes the conversion process using 
<b>OleConvertOLESTREAMToIStorage</b>.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>Converting an OLE 1 object to an OLE 2 storage object</b>

<ol>
<li>Create a root 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> object by calling the 
<a href="https://msdn.microsoft.com/3292484b-8eff-438d-b989-b58ae323872b">StgCreateDocfile</a> function (..., &amp;<i>pstg</i>).</li>
<li>Open the OLE 1 file (using <a href="https://msdn.microsoft.com/en-us/library/Mt432779(v=VS.85).aspx">OpenFile</a> or another OLE 1 technique).</li>
<li>Read from the file, using the OLE 1 procedure for reading files, until an OLE object is found.</li>
<li>Allocate an 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> object from the root 
<b>IStorage</b> created in Step 1. 


<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>pstg-&gt;lpVtbl-&gt;CreateStorage(...&amp;pStgChild); 
hRes = OleConvertIStorageToOLESTREAM(polestm, pStgChild); 
hRes = OleLoad(pStgChild, &amp;IID_IOleObject, pClientSite, ppvObj);</pre>
</td>
</tr>
</table></span></div>
</li>
<li>Repeat Step 3 until the file is completely read.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680738(v=VS.85).aspx">CoIsOle1Class</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686613(v=VS.85).aspx">DVTARGETDEVICE</a>



<a href="https://msdn.microsoft.com/d100d32a-6559-4a7c-a0ae-780bc9d82611">OleConvertIStorageToOLESTREAM</a>



<a href="https://msdn.microsoft.com/a6026b71-4223-40ab-b209-44531480db57">OleConvertIStorageToOLESTREAMEx</a>



<a href="https://msdn.microsoft.com/2e77fa0e-1d98-4c59-8d3c-65bd7235ec8f">OleConvertOLESTREAMToIStorageEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms683812(v=VS.85).aspx">STGMEDIUM</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691227(v=VS.85).aspx">TYMED</a>
 

 

