---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MsiDatabaseApplyTransformW function


## -description


The 
<b>MsiDatabaseApplyTransform</b> function applies a transform to a database.


## -parameters




### -param hDatabase [in]

Handle to the database obtained from <a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a> to the transform.


### -param szTransformFile [in]

Specifies the name of the transform file to apply.


### -param iErrorConditions [in]

Error conditions that should be suppressed. This parameter is a bit field that can contain the following bits. 



<table>
<tr>
<th>Error condition</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_ADDEXISTINGROW"></a><a id="msitransform_error_addexistingrow"></a><dl>
<dt><b>MSITRANSFORM_ERROR_ADDEXISTINGROW</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Adding a row that already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_DELMISSINGROW"></a><a id="msitransform_error_delmissingrow"></a><dl>
<dt><b>MSITRANSFORM_ERROR_DELMISSINGROW</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Deleting a row that does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_ADDEXISTINGTABLE"></a><a id="msitransform_error_addexistingtable"></a><dl>
<dt><b>MSITRANSFORM_ERROR_ADDEXISTINGTABLE</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Adding a table that already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_DELMISSINGTABLE"></a><a id="msitransform_error_delmissingtable"></a><dl>
<dt><b>MSITRANSFORM_ERROR_DELMISSINGTABLE</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Deleting a table that does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_UPDATEMISSINGROW"></a><a id="msitransform_error_updatemissingrow"></a><dl>
<dt><b>MSITRANSFORM_ERROR_UPDATEMISSINGROW</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Updating a row that does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_CHANGECODEPAGE"></a><a id="msitransform_error_changecodepage"></a><dl>
<dt><b>MSITRANSFORM_ERROR_CHANGECODEPAGE</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Transform and database code pages do not match and neither has a neutral code page.

</td>
</tr>
<tr>
<td width="40%"><a id="MSITRANSFORM_ERROR_VIEWTRANSFORM"></a><a id="msitransform_error_viewtransform"></a><dl>
<dt><b>MSITRANSFORM_ERROR_VIEWTRANSFORM</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Create the temporary 
<a href="https://msdn.microsoft.com/4763ac0e-900f-45f1-bee5-34d413c5e401">_TransformView table</a>.

</td>
</tr>
</table>
 


## -returns




					The 
<b>MsiDatabaseApplyTransform</b> function returns one of the following values:




## -remarks



The 
<b>MsiDatabaseApplyTransform</b> function delays transforming tables until it is necessary. Any tables to be added or dropped are processed immediately. However, changes to the existing table are delayed until the table is loaded or the database is committed.

An error occurs if 
<b>MsiDatabaseApplyTransform</b> is called when tables have already been loaded and saved to storage.

Because the list delimiter for transforms, sources and patches is a semicolon, this character should not be used for filenames or paths.

This function cannot be called from custom actions. A call to this function from a custom action causes the function to fail.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="database_functions.htm">Database Management Functions</a>



<a href="https://msdn.microsoft.com/525feb70-27aa-4fe2-a19f-9438168ca046">Database Transforms</a>
 

 

