---
UID: NF:shlobj_core.SHAddToRecentDocs
title: SHAddToRecentDocs function
author: windows-sdk-content
description: Notifies the system that an item has been accessed, for the purposes of tracking those items used most recently and most frequently. This function can also be used to clear all usage data.
old-location: shell\SHAddToRecentDocs.htm
tech.root: shell
ms.assetid: 84e065e6-b68d-4303-b98b-3f8507539468
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SHAddToRecentDocs, SHAddToRecentDocs function [Windows Shell], _win32_SHAddToRecentDocs, shell.SHAddToRecentDocs, shlobj_core/SHAddToRecentDocs
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHAddToRecentDocs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHAddToRecentDocs function


## -description


Notifies the system that an item has been accessed, for the purposes of tracking those items used most recently and most frequently. This function can also be used to clear all usage data.


## -parameters




### -param uFlags

Type: <b>UINT</b>

A value from the <a href="https://msdn.microsoft.com/en-us/library/Dd378453(v=VS.85).aspx">SHARD</a> enumeration that indicates the form of the information pointed to by the <i>pv</i> parameter.


### -param pv [in, optional]

Type: <b>LPCVOID</b>

A pointer to data that identifies the item that has been accessed. The item can be specified in this parameter in one of the following forms:
    
                        


<ul>
<li>A null-terminated string that contains the path and file name of the item.</li>
<li>A PIDL that identifies the item's file object.</li>
<li><b>Windows 7 and later only</b>. A <a href="https://msdn.microsoft.com/bb2b7e86-04ca-4dd0-944b-a95e8a0be1e0">SHARDAPPIDINFO</a>, <a href="https://msdn.microsoft.com/11c69ff9-b8a0-4168-8036-f45a9f7813ba">SHARDAPPIDINFOIDLIST</a>, or <a href="https://msdn.microsoft.com/01613dc9-4516-4995-bd31-feee2eb650b2">SHARDAPPIDINFOLINK</a> structure that identifies the item through an AppUserModelID. See <a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a> for more information.</li>
<li><b>Windows 7 and later only</b>. An <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> object that identifies the item through a shortcut.</li>
</ul>


Set this parameter to <b>NULL</b> to clear all usage data on all items.


## -returns



This function does not return a value.




## -remarks



The usage statistics gathered through calls to this method are used to determine lists of items accessed most recently and most frequently. These lists are seen in the <b>Start</b> menu and, in Windows 7 and later, in an application's Jump List.

When this method is called, it affects the following areas:
            
                

<ul>
<li>Updates the <b>Recent</b> and <b>Frequent</b> lists for the associated application's Jump List.</li>
<li>Adds a shortcut to the user's <a href="https://msdn.microsoft.com/d9ffda6f-adc0-44a3-b410-e23bf5f4f165">Recent</a> folder (<a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">FOLDERID_Recent</a>, <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_RECENT</a>). This is reflected in the <b>My Recent Documents</b> (Windows XP) and <b>Recent Items</b> (Windows Vista and later) menu in the <b>Start</b> menu.</li>
<li>Adds a shortcut to the Classic <b>Start</b> menu's <b>Documents</b> submenu. (Note that the Classic <b>Start</b> menu option is not available in Windows 7 and later.)</li>
</ul>
Items represented by an <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> are not added to the <b>Recent</b> folder, although they are reflected in an application's Jump List.

In some cases, notably when a user opens an item through Windows Explorer or uses the common file dialog to open, save, or create a file, the Shell calls <b>SHAddToRecentDocs</b> on behalf of the application. An application that has a custom UI for selecting items should call <b>SHAddToRecentDocs</b> explicitly to ensure accurate statistics. Duplicate calls are accounted for by the system so there is no risk of skewing the data by doing so.

Executable (.exe) files are filtered from the recently used documents list in Windows XP and later versions. Although <b>SHAddToRecentDocs</b> will accept the path of an executable file, that file will not appear in the <b>Recent Items</b> list.

Folders are also accepted by <b>SHAddToRecentDocs</b>, but appear only in the Jump List for the Windows Explorer taskbar button. Folders do not appear in any other application's Jump List.

In certain cases, <b>SHAddToRecentDocs</b> attempts to register an application to handle a file type that it is not registered to handle. This occurs under these circumstances:

<ul>
<li>An application explicitly calls <b>SHAddToRecentDocs</b> with a file type that it is not registered to handle. This also applies to calls made to <b>SHAddToRecentDocs</b> by the common file dialog on behalf of the application, but only when the dialog is used to open a file, not when it is used to save one.</li>
<li>The user drops a file of a type that the application is not registered to handle on the application's taskbar button.</li>
</ul>
This registration is done per-user.

A set of requirements must be met for the registration to be accomplished successfully:

<ul>
<li>The application must be registered under <b>HKEY_CLASSES_ROOT</b>\<b>Applications</b>.</li>
<li>That registration cannot include the NoOpenWith value. See <a href="https://msdn.microsoft.com/055648cd-46ce-4e61-80b2-bcf1d1823e20">File Types</a> for more details on NoOpenWith.</li>
<li>That registration cannot supply data under a <b>SupportedTypes</b> subkey. See <a href="https://msdn.microsoft.com/055648cd-46ce-4e61-80b2-bcf1d1823e20">File Types</a> for more details on the <b>SupportedTypes</b> subkey.</li>
<li>
The application's executable file cannot be listed in the KillList value found here:


<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>Explorer</b>
                  <b>FileAssociation</b>
                     <b>KillList</b></pre>


<div class="alert"><b>Note</b>  Third party applications should not modify the KillList value. It should be regarded as read-only.</div>
<div> </div>
</li>
<li>
The application's <b>HKEY_CLASSES_ROOT</b>\<b>Applications</b> registration must have a set of default verbs defined under a 
                        
                            
                            <b>HKEY_CLASSES_ROOT</b>\<b>Applications</b>\<i>ExampleApp.exe</i>\<b>shell</b> subkey.
                        

If <b>SHAddToRecentDocs</b> is attempting the registration as the result of a drag-and-drop onto the taskbar button, the <b>shell</b> subkey is created if it does not already exist, as long as the existing application registration does not contain a NoOpenWith value and the application's executable is not listed in the KillList value.

</li>
</ul>
<h3><a id="Suppressing_Calls_to_SHAddToRecentDocs"></a><a id="suppressing_calls_to_shaddtorecentdocs"></a><a id="SUPPRESSING_CALLS_TO_SHADDTORECENTDOCS"></a>Suppressing Calls to SHAddToRecentDocs</h3>
In versions of Windows before Windows 7, a file type could set the <a href="https://msdn.microsoft.com/en-us/library/Bb762506(v=VS.85).aspx">FTA_NoRecentDocs</a> flag to prevent that file type from being added to the <b>Recent</b> folder. This mechanism is also supported under Windows 7 and later. See <a href="https://msdn.microsoft.com/055648cd-46ce-4e61-80b2-bcf1d1823e20">File Types</a> for more information.

<b>SHAddToRecentDocs</b> tracks document usage statistics through the verbs that are invoked to access those documents. Verbs supplied by registered <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> handlers are tracked, those items appear in <b>My Recent Documents</b> (Windows XP) and <b>Recent Items</b> (Windows Vista). In Windows 7, the parent folders of the documents appear in the Jump List for the Windows Explorer taskbar button. However, the documents accessed through those <b>IContextMenu</b> verbs do not appear in application Jump Lists. For those items to appear in an application's Jump List, an application must call <b>SHAddToRecentDocs</b> explicitly.

Prior to Windows 7, only the <code>open</code> verb resulted in a call to <b>SHAddToRecentDocs</b>. In Windows 7 and later, other verbs can also generate usage statistics. This information is used to make a Jump List's destinations more complete and accurate.

However, some classes of file type association registrations or individual <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> implementations are not appropriate for this sort of tracking. The point of usage tracking is to generate a list of items that the user is likely to want to access again. If a particular verb—<code>delete</code>, for instance—is inherently invoked on an item that the user will not access again, or is a secondary action such as a virus scan on a file, that verb is not appropriate for tracking. File type classes should remove themselves from this tracking through the registry entry NoRecentDocs. NoRecentDocs is of type REG_SZ and has no associated data. Its presence is all that is required to prevent the call to <b>SHAddToRecentDocs</b>.

For example, context menu extensions and static verbs registered under <b>HKEY_CLASSES_ROOT</b> in classes such as "*", "AllFileSystemObjects", or "Folder" should not be tracked. In cases such as these, the NoRecentDocs entry is added to the root of the class key as shown here to suppress tracking of documents launched through any verb or extension registered to that class:


<pre xml:space="preserve"><b>HKEY_CLASSES_ROOT</b>
   <b>AllFileSystemObjects</b>
      <b>NoRecentDocs</b></pre>


The NoRecentDocs entry is assigned by default to the <b>*</b>, <b>AllFileSystemObjects</b>, <b>Folder</b>, <b>Directory</b>, and <b>DesktopBackground</b> class subkeys.

Individual <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> implementations can opt out of tracking by adding a NoRecentDocs subkey to its Component Object Model (COM) object's registration, in its <b>shellex</b> subkey, as shown here:


<pre xml:space="preserve"><b>HKEY_CLASSES_ROOT</b>
   <b>CLSID</b>
      <i>{093C7AAB-5E72-454f-A91D-CA1BC991FCEC}</i>
         <b>shellex</b>
            <b>NoRecentDocs</b></pre>


This subkey is not present by default on any <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> implementation.




## -see-also




<a href="https://msdn.microsoft.com/6fcac066-1ab0-443a-9994-b68ead3bbc20">SHGetFolderLocation</a>



<a href="https://msdn.microsoft.com/a240abc0-e0a6-4f95-8e74-7dc410970212">SHGetFolderPath</a>
 

 

