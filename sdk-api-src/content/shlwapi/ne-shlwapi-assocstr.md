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

# ASSOCSTR enumeration


## -description


Used by <a href="https://msdn.microsoft.com/72463664-783b-4375-a6ba-43633a82ec7e">IQueryAssociations::GetString</a> to define the type of string that is to be returned.


## -enum-fields




### -field ASSOCSTR_COMMAND

A command string associated with a Shell verb.


### -field ASSOCSTR_EXECUTABLE

An executable from a Shell verb command string. For example, this string is found as the (Default) value for a subkey such as 
                    
                        <b>HKEY_CLASSES_ROOT</b>\<i>ApplicationName</i>\<b>shell</b>\<b>Open</b>\<b>command</b>. If the command uses Rundll.exe, set the <b>ASSOCF_REMAPRUNDLL</b> flag in the <i>flags</i> parameter of <a href="https://msdn.microsoft.com/72463664-783b-4375-a6ba-43633a82ec7e">IQueryAssociations::GetString</a> to retrieve the target executable.

<div class="alert"><b>Caution</b>  <p class="note">Not all app associations have executables. Do not assume that an executable will always be present.

</div>
<div> </div>
This type of string will identify the code that will be invoked in the implementation of the verb.


### -field ASSOCSTR_FRIENDLYDOCNAME

The friendly name of a document type.


### -field ASSOCSTR_FRIENDLYAPPNAME

The friendly name of an executable file.


### -field ASSOCSTR_NOOPEN

Ignore the information associated with the <b>open</b> subkey.


### -field ASSOCSTR_SHELLNEWVALUE

Look under the <b>ShellNew</b> subkey.


### -field ASSOCSTR_DDECOMMAND

A template for DDE commands.


### -field ASSOCSTR_DDEIFEXEC

The DDE command to use to create a process.


### -field ASSOCSTR_DDEAPPLICATION

The application name in a DDE broadcast.


### -field ASSOCSTR_DDETOPIC

The topic name in a DDE broadcast.


### -field ASSOCSTR_INFOTIP

Corresponds to the InfoTip registry value. Returns an info tip for an item, or list of properties in the form of an <a href="https://msdn.microsoft.com/e0530195-27da-4df7-884f-518e905f3c0e">IPropertyDescriptionList</a> from which to create an info tip, such as when hovering the cursor over a file name. The list of properties can be parsed with <a href="https://msdn.microsoft.com/348253ed-46ac-4643-bbf8-2d286ae97f07">PSGetPropertyDescriptionListFromString</a>.


### -field ASSOCSTR_QUICKTIP

<b>Introduced in Internet Explorer 6</b>. Corresponds to the QuickTip registry value. Same as ASSOCSTR_INFOTIP, except that it always returns a list of property names in the form of an <a href="https://msdn.microsoft.com/e0530195-27da-4df7-884f-518e905f3c0e">IPropertyDescriptionList</a>. The difference between this value and ASSOCSTR_INFOTIP is that this returns properties that are safe for any scenario that causes slow property retrieval, such as offline or slow networks. Some of the properties returned from ASSOCSTR_INFOTIP might not be appropriate for slow property retrieval scenarios. The list of properties can be parsed with <a href="https://msdn.microsoft.com/348253ed-46ac-4643-bbf8-2d286ae97f07">PSGetPropertyDescriptionListFromString</a>.


### -field ASSOCSTR_TILEINFO

<b>Introduced in Internet Explorer 6</b>. Corresponds to the TileInfo registry value. Contains a list of properties to be displayed for a particular file type in a Windows Explorer window that is in tile view. This is the same as ASSOCSTR_INFOTIP, but, like ASSOCSTR_QUICKTIP, it also returns a list of property names in the form of an <a href="https://msdn.microsoft.com/e0530195-27da-4df7-884f-518e905f3c0e">IPropertyDescriptionList</a>. The list of properties can be parsed with <a href="https://msdn.microsoft.com/348253ed-46ac-4643-bbf8-2d286ae97f07">PSGetPropertyDescriptionListFromString</a>.


### -field ASSOCSTR_CONTENTTYPE

<b>Introduced in Internet Explorer 6</b>. Describes a general type of MIME file association, such as image and bmp, so that applications can make general assumptions about a specific file type.


### -field ASSOCSTR_DEFAULTICON

<b>Introduced in Internet Explorer 6</b>. Returns the path to the icon resources to use by default for this association. Positive numbers indicate an index into the dll's resource table, while negative numbers indicate a resource ID. An example of the syntax for the resource is "c:\myfolder\myfile.dll,-1".


### -field ASSOCSTR_SHELLEXTENSION

<b>Introduced in Internet Explorer 6</b>. For an object that has a Shell extension associated with it, you can use this to retrieve the CLSID of that Shell extension object by passing a string representation of the IID of the interface you want to retrieve as the <i>pwszExtra</i> parameter of <a href="https://msdn.microsoft.com/72463664-783b-4375-a6ba-43633a82ec7e">IQueryAssociations::GetString</a>. For example, if you want to retrieve a handler that implements the <a href="https://msdn.microsoft.com/28a13749-89e7-407e-89cb-95464859ce3e">IExtractImage</a> interface, you would specify "{BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}", which is the IID of <b>IExtractImage</b>.


### -field ASSOCSTR_DROPTARGET

<b>Introduced in Internet Explorer 8</b>.. For a verb invoked through COM and the <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interface, you can use this flag to retrieve the <b>IDropTarget</b> object's CLSID. This CLSID is registered in the <b>DropTarget</b> subkey. The verb is specified in the <i>pwszExtra</i> parameter in the call to <a href="https://msdn.microsoft.com/72463664-783b-4375-a6ba-43633a82ec7e">IQueryAssociations::GetString</a>.

This type of string will identify the code that will be invoked in the implementation of the verb.


### -field ASSOCSTR_DELEGATEEXECUTE

<b>Introduced in Internet Explorer 8</b>.. For a verb invoked through COM and the <a href="https://msdn.microsoft.com/a3432f1a-dd33-4e0d-8b26-1312bb5151f7">IExecuteCommand</a> interface, you can use this flag to retrieve the <b>IExecuteCommand</b> object's CLSID. This CLSID is registered in the verb's <b>command</b> subkey as the DelegateExecute entry. The verb is specified in the <i>pwszExtra</i> parameter in the call to <a href="https://msdn.microsoft.com/72463664-783b-4375-a6ba-43633a82ec7e">IQueryAssociations::GetString</a>.

This type of string will identify the code that will be invoked in the implementation of the verb.


### -field ASSOCSTR_SUPPORTED_URI_PROTOCOLS

<b>Introduced in Windows 8</b>. 


### -field ASSOCSTR_PROGID

The ProgID provided by the app associated with the file type or URI scheme. This if configured by users in their default program settings.


### -field ASSOCSTR_APPID

The AppUserModelID of the app associated with the file type or URI scheme. This is configured by users in their default program settings.


### -field ASSOCSTR_APPPUBLISHER

The publisher of the app associated with the file type or URI scheme. This is configured by users in their default program settings.


### -field ASSOCSTR_APPICONREFERENCE

The icon reference of the app associated with the file type or URI scheme. This is configured by users in their default program settings.


### -field ASSOCSTR_MAX

The maximum defined ASSOCSTR value, used for validation purposes.

