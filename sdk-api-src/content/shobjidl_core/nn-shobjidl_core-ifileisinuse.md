---
UID: NN:shobjidl_core.IFileIsInUse
title: IFileIsInUse (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that can be called to get information on or close a file that is in use by another application.
old-location: shell\IFileIsInUse.htm
tech.root: shell
ms.assetid: 68a4ab3d-165e-4917-8915-77f15901dbad
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFileIsInUse, IFileIsInUse interface [Windows Shell], IFileIsInUse interface [Windows Shell],described, _shell_IFileIsInUse, shell.IFileIsInUse, shobjidl_core/IFileIsInUse
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileIsInUse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileIsInUse interface


## -description


Exposes methods that can be called to get information on or close a file that is in use by another application. When an application attempts to access a file and finds that file already in use, it can use the methods of this interface to gather information to present to the user in a dialog box.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileIsInUse</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFileIsInUse</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileIsInUse</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27338e5a-b303-4b72-b316-3059ec6f1698">CloseFile</a>
</td>
<td align="left" width="63%">
Closes the file currently in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/282334a9-28b4-4c3f-977e-824011efe381">GetAppName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the application that is using the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2ce674a-4c06-401d-bfb0-bc2a086ef89c">GetCapabilities</a>
</td>
<td align="left" width="63%">
Determines whether the file can be closed and whether the UI is capable of switching to the window of the application that is using the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4223cb0-2027-4073-9558-99ae27f4e52a">GetSwitchToHWND</a>
</td>
<td align="left" width="63%">
Retrieves the handle of the top-level window of the application that is using the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7baba34d-b246-4d48-9f0c-e950d33ed5cf">GetUsage</a>
</td>
<td align="left" width="63%">
Gets a value that indicates how the file in use is being used.

</td>
</tr>
</table> 


## -remarks



In versions of Windows before Windows Vista, when a user attempted to access a file that was open in another application, the user would simply receive a dialog box with a message stating that the file was already open. The message instructed that the user close the other application, but did not identify it. Other than that suggestion, the dialog box provided no user action to address the situation. This interface provides methods that can lead to a more informative dialog box from which the user can take direct action.

<h3><a id="The_Running_Object_Table"></a><a id="the_running_object_table"></a><a id="THE_RUNNING_OBJECT_TABLE"></a>The Running Object Table</h3>
When an application opens a file, that application registers the file by inserting the instantiated <b>IFileIsInUse</b> object into the running object table (ROT). The ROT is a globally accessible lookup table that keeps track of currently running objects. These objects can be identified by a moniker. When a client attempts to bind a moniker to an object, the moniker checks the ROT to determine whether the object is already running. This allows the moniker to bind to the current instance rather than loading a new instance.

Perform these steps to add a file to the ROT:


<ol>
<li>Call the <a href="https://msdn.microsoft.com/65d9cf7d-cc8a-4199-9a4a-7fd67ef8872d">GetRunningObjectTable</a> function to retrieve an instance of <a href="https://msdn.microsoft.com/ff89bcb5-df6d-4325-b0e8-613217a68f42">IRunningObjectTable</a>.</li>
<li>Create an <b>IFileIsInUse</b> object for the file that is currently in use.</li>
<li>Create an <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> object for the file that is currently in use.</li>
<li>Insert the <b>IFileIsInUse</b> and <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> objects into the ROT by calling <a href="https://msdn.microsoft.com/40f815b2-dfea-416c-aae1-7ba3a710ad91">IRunningObjectTable::Register</a>.</li>
</ol>


In the call to <a href="https://msdn.microsoft.com/40f815b2-dfea-416c-aae1-7ba3a710ad91">Register</a>, specify the <b>ROTFLAGS_ALLOWANYCLIENT</b> flag. This allows the ROT entry to work across security boundaries. Use of this flag requires the calling application to have an explicit Application User Model ID (AppUserModelID) (<a href="https://msdn.microsoft.com/07858b3c-e601-40ec-a87a-d66612d5473a">System.AppUserModel.ID</a>). An explicit AppUserModelID allows the Component Object Model (COM) to inspect the application's security settings. An attempt to call <b>Register</b> with ROTFLAGS_ALLOWANYCLIENT and no explicit AppUserModelID will fail. You can call <b>Register</b> without the ROTFLAGS_ALLOWANYCLIENT flag and the application will work correctly, but only within its own security level.

The value retrieved in the <a href="https://msdn.microsoft.com/40f815b2-dfea-416c-aae1-7ba3a710ad91">Register</a> method's [out] parameter is used to identify the entry in later calls to retrieve or remove it from the ROT.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Applications that open file types that can be opened by other applications should implement <b>IFileIsInUse</b>. An application's implementation of this interface enables Windows Explorer to discover the source of sharing errors, which enables users to address and retry operations that fail due to those errors.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
An application calls <b>IFileIsInUse</b> to communicate with other applications to resolve sharing errors. These errors occur in response to user action in the file system. For example, when a user attempts to rename a folder while a file in that folder is open in an application, the renaming operation fails. Windows Explorer can call that appplication's implementation of <b>IFileIsInUse</b> to help the user identify the conflict and resolve this issue.

<h3><a id="Sample"></a><a id="sample"></a><a id="SAMPLE"></a>Sample</h3>
See the <a href="https://msdn.microsoft.com/22EFE7CC-D223-46b3-BD6B-293E3FA0BA01">File Is in Use</a> sample, which demonstrates how to implement <b>IFileIsInUse</b> and register a file with the ROT. It then shows how to customize the <b>File In Use</b> dialog to display additional information and options for files currently opened in an application.




## -see-also




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a>
 

 

