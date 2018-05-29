---
UID: NF:ole2.OleSave
title: OleSave function
author: windows-sdk-content
description: Saves an object opened in transacted mode into the specified storage object.
old-location: com\olesave.htm
old-project: com
ms.assetid: b8d8e1af-05a3-42f5-8672-910a2606e613
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: OleSave, OleSave function [COM], _ole_OleSave, com.olesave, ole2/OleSave
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
-	OleSave
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OleSave function


## -description


Saves an object opened in transacted mode into the specified storage object.


## -parameters




### -param pPS [in]

Pointer to the <a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a> interface on the object to be saved.


### -param pStg [in]

Pointer to the <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the destination storage object to which the object indicated in <i>pPS</i> is to be saved.


### -param fSameAsLoad [in]

<b>TRUE</b> indicates that <i>pStg</i> is the same storage object from which the object was loaded or created; <b>FALSE</b> indicates that <i>pStg</i> was loaded or created from a different storage object.


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
<dt><b>STGMEDIUM_E_FULL</b></dt>
</dl>
</td>
<td width="60%">
The object could not be saved due to lack of disk space.

This function can also return any of the error values returned by the <a href="https://msdn.microsoft.com/3a200812-48d9-4202-987a-1400aa66191c">IPersistStorage::Save</a> method.

</td>
</tr>
</table>
 




## -remarks



The <b>OleSave</b> helper function handles the common situation in which an object is open in transacted mode and is then to be saved into the specified storage object which uses the OLE-provided compound file implementation. Transacted mode means that changes to the object are buffered until either of the <a href="https://msdn.microsoft.com/72831f2c-1e07-429b-af4c-2aaced3f3888">IStorage::Commit</a> or <a href="https://msdn.microsoft.com/d1b7626e-bad1-47b5-8bcd-3da3b05c53c4">IStorage::Revert</a> is called. Callers can handle other situations by calling the <a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a> and <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interfaces directly.



<b>OleSave</b> does the following: 

<ul>
<li>Calls the <a href="https://msdn.microsoft.com/921a3b86-a240-454e-9411-8d653e02b90e">IPersist::GetClassID</a> method to get the CLSID of the object.</li>
<li>Writes the CLSID to the storage object using the <a href="https://msdn.microsoft.com/5f2f16d1-923f-4ba7-8d4b-7e8535f6f15e">WriteClassStg</a> function. 
</li>
<li>Calls the <a href="https://msdn.microsoft.com/3a200812-48d9-4202-987a-1400aa66191c">IPersistStorage::Save</a> method to save the object.
</li>
<li>If there were no errors on the save; calls the <a href="https://msdn.microsoft.com/72831f2c-1e07-429b-af4c-2aaced3f3888">IStorage::Commit</a> method to commit the changes.
</li>
</ul>
<div class="alert"><b>Note</b>  Static objects are saved into a stream called CONTENTS. Static metafile objects get saved in "placeable metafile format" and static DIB data gets saved in "DIB file format." These formats are defined to be the OLE standards for metafile and DIB. All data transferred using an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface or a file (that is, via <a href="https://msdn.microsoft.com/802fc49a-21c2-4490-9b00-1359ce9c325f">IDataObject::GetDataHere</a>) must be in these formats. Also, all objects whose default file format is a metafile or DIB must write their data into a CONTENTS stream using these standard formats.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a>



<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>
 

 

