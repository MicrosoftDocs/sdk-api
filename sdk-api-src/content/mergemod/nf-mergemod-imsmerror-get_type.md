---
UID: NF:mergemod.IMsmError.get_Type
title: IMsmError::get_Type
author: windows-sdk-content
description: The get_Type method retrieves the Type property of the Error object. This method returns a msmErrorType value indicating the type of error represented by this object.
old-location: setup\imsmerror_get_type.htm
tech.root: msi
ms.assetid: 733a5390-419d-414a-b50e-8400d179bfb6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMsmError interface,get_Type method, IMsmError.get_Type, IMsmError::get_Type, _msi_get_type_function_error_object_, get_Type, get_Type method, get_Type method,IMsmError interface, mergemod/IMsmError::get_Type, setup.imsmerror_get_type
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 2.0 or later
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmError.get_Type
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmError::get_Type


## -description


The 
<b>get_Type</b> method retrieves the 
<a href="https://msdn.microsoft.com/5567ba71-c815-4434-962c-aa46cd171712">Type</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object. This method returns a msmErrorType value indicating the type of error represented by this object.


## -parameters




### -param ErrorType [out]

A pointer to a location in memory that receives the type of error.
					

<table>
<tr>
<th>msmErrorType</th>
<th>Value</th>
<th><b>Description</b></th>
</tr>
<tr>
<td>msmErrorLanguageUnsupported</td>
<td>1</td>
<td>A request was made to open a module with a language not supported by the module. No more general language is supported by the module. Adds msmErrorLanguageUnsupported to the 
<b>Type</b> property and the requested language to the 
<a href="https://msdn.microsoft.com/f47cad5d-8e76-4210-b1ab-377d2d05379e">Language Property (Error Object)</a>. All <b>Error</b> object properties are empty. The 
<a href="https://msdn.microsoft.com/37225e61-c24f-4a44-8fdf-673590a6e09d">OpenModule</a> function returns ERROR_INSTALL_LANGUAGE_UNSUPPORTED (as HRESULT).</td>
</tr>
<tr>
<td>msmErrorLanguageFailed</td>
<td>2</td>
<td>A request was made to open a module with a supported language but the module has an invalid language transform. Adds msmErrorLanguageFailed to the Type property and the applied transform's language to the 
<b>Language</b> Property of the <b>Error</b> object. This may not be the requested language if a more general language was used. All other properties of the <b>Error</b> object are empty. The 
<b>OpenModule</b> function returns ERROR_INSTALL_LANGUAGE_UNSUPPORTED (as HRESULT).</td>
</tr>
<tr>
<td>msmErrorExclusion</td>
<td>3</td>
<td>The module cannot be merged because it excludes, or is excluded by, another module in the database. Adds msmErrorExclusion to the 
<b>Type</b> property of the <b>Error</b> object. The 
<a href="https://msdn.microsoft.com/b02b609b-4682-4228-b29a-364f079e863c">ModuleKeys property</a> or 
<a href="https://msdn.microsoft.com/416a6cef-4c70-4c06-a8d2-801c9440e25a">DatabaseKeys property</a> contains the primary keys of the excluded module's row in the 
<a href="https://msdn.microsoft.com/c28d9afa-152c-43b5-9892-7a38fae8c593">ModuleExclusion table</a>. If an existing module excludes the module being merged, the excluded module's ModuleSignature information is added to ModuleKeys. If the module being merged excludes an existing module, DatabaseKeys contains the excluded module's ModuleSignature information. All other properties are empty (or -1).</td>
</tr>
<tr>
<td>msmErrorTableMerge</td>
<td>4</td>
<td>Merge conflict during merge. The value of the 
<b>Type</b> property is set to msmErrorTableMerge. The 
<a href="https://msdn.microsoft.com/38ff45ca-4bd6-43f3-88ad-db4077daeb77">DatabaseTable property</a> and 
<a href="https://msdn.microsoft.com/416a6cef-4c70-4c06-a8d2-801c9440e25a">DatabaseKeys property</a> contain the table name and primary keys of the conflicting row in the database. The 
<a href="https://msdn.microsoft.com/390f5889-d638-4c1c-b95c-76d38c934e7c">ModuleTable property</a> and 
<a href="https://msdn.microsoft.com/b02b609b-4682-4228-b29a-364f079e863c">ModuleKeys property</a> contain the table name and primary keys of the conflicting row in the module. The ModuleTable and ModuleKeys entries may be null if the row does not exist in the database. For example, if the conflict is in a generated FeatureComponents table entry. When merging a 
<a href="https://msdn.microsoft.com/461436f0-3a91-4a49-934a-f975bf13df40">configurable merge module</a>, configuration may cause these properties to refer to rows that do not exist in the module.</td>
</tr>
<tr>
<td>msmErrorResequenceMerge</td>
<td>5</td>
<td>There was a problem resequencing a sequence table to contain the necessary merged actions. The 
<b>Type</b> property is set to msmErrorResequenceMerge. The DatabaseTable and DatabaseKeys properties contain the sequence table name and primary keys (action name) of the conflicting row. The ModuleTable and ModuleKeys properties contain the sequence table name and primary key (action name) of the conflicting row. When merging a configurable merge module, configuration may cause these properties to refer to rows that do not exist in the module.</td>
</tr>
<tr>
<td>msmErrorFileCreate</td>
<td>6</td>
<td>Not used.</td>
</tr>
<tr>
<td>msmErrorDirCreate</td>
<td>7</td>
<td>There was a problem creating a directory to extract a file to disk. The 
<a href="https://msdn.microsoft.com/b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b">Path</a> property contains the directory that could not be created. All other properties are empty or -1. </td>
</tr>
<tr>
<td>msmErrorFeatureRequired</td>
<td>8</td>
<td>A feature name is required to complete the merge, but no feature name was provided. The 
<b>Type</b> property is set to msmErrorFeatureRequired. The DatabaseTable and DatabaseKeys contain the table name and primary keys of the conflicting row. The ModuleTable and ModuleKeys properties contain the table name and primary keys of the row cannot be merged. When merging a configurable merge module, configuration may cause these properties to refer to rows that do not exist in the module. If the failure is in a generated 
<a href="https://msdn.microsoft.com/aff16483-a9ed-4675-8e87-8adf695605ee">FeatureComponents table</a>, the DatabaseTable and DatabaseKeys properties are empty and the ModuleTable and ModuleKeys properties refer to the row in the 
<a href="https://msdn.microsoft.com/069d64e9-106a-42b7-8dea-a44fc0c6e0cd">Component table</a> causing the failure.</td>
</tr>
<tr>
<td>msmErrorBadNullSubstitution</td>
<td>9</td>
<td>Substitution of a Null value into a non-nullable column. This enters msmErrorBadNullSubstitution in the 
<b>Type</b> property and enters "ModuleSubstitution" and the keys from the 
<a href="https://msdn.microsoft.com/8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400">ModuleSubstitution table</a> for this row into the 
<a href="https://msdn.microsoft.com/390f5889-d638-4c1c-b95c-76d38c934e7c">ModuleTable</a> property and 
<a href="https://msdn.microsoft.com/b02b609b-4682-4228-b29a-364f079e863c">ModuleKeys</a> property. All other properties of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object are set to an empty string or -1. 


This error causes the immediate failure of the merge and the 
<b>MergeEx</b>
<a href="https://msdn.microsoft.com/fdfd950f-cba9-4b87-ae07-c3d3b127f69d">function</a> to return E_FAIL.

</td>
</tr>
<tr>
<td>msmErrorBadSubstitutionType</td>
<td>10</td>
<td>Substitution of 
<a href="https://msdn.microsoft.com/71b89f87-43ba-41cd-a969-765d45da4ba4">Text Format Type</a> or 
<a href="https://msdn.microsoft.com/63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d">Integer Format Type</a> into a 
<a href="https://msdn.microsoft.com/b6a25100-9f3e-4207-b56f-0c27ee16f188">Binary Type</a> data column. This type of error returns msmErrorBadSubstitutionType in the 
<b>Type</b> property and enters "ModuleSubstitution" and the keys from the 
<a href="https://msdn.microsoft.com/8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400">ModuleSubstitution table</a> for this row into the 
<a href="https://msdn.microsoft.com/390f5889-d638-4c1c-b95c-76d38c934e7c">ModuleTable</a> property. All other properties of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object are set to an empty string or -1. 


This error causes the immediate failure of the merge and the 
<b>MergeEx</b>
<a href="https://msdn.microsoft.com/fdfd950f-cba9-4b87-ae07-c3d3b127f69d">function</a> to return E_FAIL.

</td>
</tr>
<tr>
<td>msmErrorMissingConfigItem</td>
<td>11</td>
<td>A row in the 
<a href="https://msdn.microsoft.com/8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400">ModuleSubstitution table</a> references a configuration item not defined in the 
<a href="https://msdn.microsoft.com/3b77cc23-c104-4adc-868c-3aa2b5794bc7">ModuleConfiguration table</a>. This type of error returns msmErrorMissingConfigItem in the 
<b>Type</b> property and enters "ModuleSubstitution" and the keys from the 
<a href="https://msdn.microsoft.com/8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400">ModuleSubstitution table</a> for this row into the 
<a href="https://msdn.microsoft.com/390f5889-d638-4c1c-b95c-76d38c934e7c">ModuleTable</a> property. All other properties of the <b>Error</b>object are set to an empty string or -1. 


This error causes the immediate failure of the merge and the 
<b>MergeEx</b>
<a href="https://msdn.microsoft.com/fdfd950f-cba9-4b87-ae07-c3d3b127f69d">function</a> to return E_FAIL.

</td>
</tr>
<tr>
<td>msmErrorBadNullResponse</td>
<td>12</td>
<td>The authoring tool has returned a Null value for an item marked with the msmConfigItemNonNullable attribute. An error of this type returns msmErrorBadNullResponse in the 
<b>Type</b> property and enters "ModuleSubstitution" and the keys from the 
<a href="https://msdn.microsoft.com/8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400">ModuleSubstitution table</a> for for the item into the 
<a href="https://msdn.microsoft.com/390f5889-d638-4c1c-b95c-76d38c934e7c">ModuleTable</a> property. All other properties of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object are set to an empty string or -1. 


This error causes the immediate failure of the merge and the 
<b>MergeEx</b>
<a href="https://msdn.microsoft.com/fdfd950f-cba9-4b87-ae07-c3d3b127f69d">function</a> to return E_FAIL.

</td>
</tr>
<tr>
<td>msmErrorDataRequestFailed</td>
<td>13</td>
<td>The authoring tool returned a failure code (not S_OK or S_FALSE) when asked for data. An error of this type will return msmErrorDataRequestFailed in the 
<b>Type</b> property and enters "ModuleSubstitution" and the keys from the 
<a href="https://msdn.microsoft.com/8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400">ModuleSubstitution table</a> for the item into the 
<a href="https://msdn.microsoft.com/390f5889-d638-4c1c-b95c-76d38c934e7c">ModuleTable</a> property. All other properties of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object are set to an empty string or -1. 


This error causes the immediate failure of the merge and the 
<b>MergeEx</b>
<a href="https://msdn.microsoft.com/fdfd950f-cba9-4b87-ae07-c3d3b127f69d">function</a> to return E_FAIL.

</td>
</tr>
<tr>
<td>msmErrorPlatformMismatch</td>
<td>14</td>
<td>Indicates that an attempt was made to merge a 64-bit module into a package that was not a 64-bit package. An error of this type returns msmErrorPlatformMismatch in the 
<b>Type</b> property. All other properties of the error object are set to an empty string or -1. This error causes the immediate failure of the merge and causes the 
<a href="https://msdn.microsoft.com/3ff1a2a8-accb-43d7-ba38-a89a5d099dc5">Merge</a> function or 
<a href="https://msdn.microsoft.com/fdfd950f-cba9-4b87-ae07-c3d3b127f69d">MergeEx</a> function to return E_FAIL.</td>
</tr>
</table>
 


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
ErrorType is Null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

