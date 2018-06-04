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

# NPPropertyDialog function


## -description


Called when the user clicks a button added by using the <b>NPPropertyDialog</b> function. The <b>NPPropertyDialog</b> function is called only for file and directory network properties.


## -parameters




### -param hwndParent [in]

A handle to the parent window that should own the file property dialog box.


### -param iButtonDlg [in]

The index of the button that was pressed. 




This index specifies which property dialog box was requested, starting with one for the first button returned from 
the <a href="https://msdn.microsoft.com/5c4583f5-81e9-4723-8fd0-6909b0107446">NPGetPropertyText</a> function. If there are multiple file names selected, 10 is added to this number. In other words, if there is more than one file selected and the user presses the first provider-defined property button, <i>iButtonDlg</i> will be 11. If there is only one file selected and the user presses the second network property button, <i>iButtonDlg</i> will be two.


### -param nPropSel [in]

Specifies what items the property dialog box should act on. This parameter can be one of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WNPS_FILE"></a><a id="wnps_file"></a><dl>
<dt><b>WNPS_FILE</b></dt>
</dl>
</td>
<td width="60%">
A single file.

</td>
</tr>
<tr>
<td width="40%"><a id="WNPS_DIR"></a><a id="wnps_dir"></a><dl>
<dt><b>WNPS_DIR</b></dt>
</dl>
</td>
<td width="60%">
A single directory.

</td>
</tr>
<tr>
<td width="40%"><a id="WNPS_MULT"></a><a id="wnps_mult"></a><dl>
<dt><b>WNPS_MULT</b></dt>
</dl>
</td>
<td width="60%">
A selection of multiple files, directories, or both.

</td>
</tr>
</table>
 


### -param lpFileName [in]

A pointer to the names of the items that the property dialog box should act on. The only supported items are files and directories, so the item names are file names. These should be unambiguous, contain no wildcard characters, and  be fully qualified, for example, <b>C:\Local\</b><i>Example</i><b>.doc</b>. Multiple file names should be separated with spaces. A file name that contains spaces can be enclosed in quotation marks, for example, <b>"C:\</b><i>My File</i><b>"</b>. In this case, it is treated as a single name. A caret  (^) can also be used as the quotation mechanism for single characters, for example, C:\My^"File and  "C:\My^"File" both refer to the file C:\My"File.


### -param nType [in]

Specifies the item type, which must be WNTYPE_FILE.


## -returns




						If the function succeeds, it returns WN_SUCCESS. If the function fails, it returns an error code. Call 
<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to set this extended error code, which may include the following return codes.
					

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_VALUE</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters is an unexpected form or value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to display the dialog box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network error occurred.

</td>
</tr>
</table>
 




## -remarks



This function is  called only on sets of properties for which 
<a href="https://msdn.microsoft.com/5c4583f5-81e9-4723-8fd0-6909b0107446">NPGetPropertyText</a> has assigned a button name.

This function is used in File Manager to view and modify the network properties (for example, permissions) for files on a network device. If this function is not supported, File Manager does not provide any default behavior.

In this version of the Network Provider interface, <i>lpFileName</i> can point to only file names. The network provider should return WN_BAD_VALUE if it sees an inappropriate device.




## -see-also




<a href="https://msdn.microsoft.com/5c4583f5-81e9-4723-8fd0-6909b0107446">NPGetPropertyText</a>



<a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a>
 

 

