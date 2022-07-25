---
UID: NE:shlwapi.__unnamed_enum_6
title: ASSOCSTR (shlwapi.h)
description: Used by IQueryAssociations::GetString to define the type of string that is to be returned.
helpviewer_keywords: ["ASSOCSTR","ASSOCSTR enumeration [Windows Shell]","ASSOCSTR_APPICONREFERENCE","ASSOCSTR_APPID","ASSOCSTR_APPPUBLISHER","ASSOCSTR_COMMAND","ASSOCSTR_CONTENTTYPE","ASSOCSTR_DDEAPPLICATION","ASSOCSTR_DDECOMMAND","ASSOCSTR_DDEIFEXEC","ASSOCSTR_DDETOPIC","ASSOCSTR_DEFAULTICON","ASSOCSTR_DELEGATEEXECUTE","ASSOCSTR_DROPTARGET","ASSOCSTR_EXECUTABLE","ASSOCSTR_FRIENDLYAPPNAME","ASSOCSTR_FRIENDLYDOCNAME","ASSOCSTR_INFOTIP","ASSOCSTR_MAX","ASSOCSTR_NOOPEN","ASSOCSTR_PROGID","ASSOCSTR_QUICKTIP","ASSOCSTR_SHELLEXTENSION","ASSOCSTR_SHELLNEWVALUE","ASSOCSTR_SUPPORTED_URI_PROTOCOLS","ASSOCSTR_TILEINFO","_win32_ASSOCSTR_str","shell.ASSOCSTR_str","shlwapi/ASSOCSTR","shlwapi/ASSOCSTR_APPICONREFERENCE","shlwapi/ASSOCSTR_APPID","shlwapi/ASSOCSTR_APPPUBLISHER","shlwapi/ASSOCSTR_COMMAND","shlwapi/ASSOCSTR_CONTENTTYPE","shlwapi/ASSOCSTR_DDEAPPLICATION","shlwapi/ASSOCSTR_DDECOMMAND","shlwapi/ASSOCSTR_DDEIFEXEC","shlwapi/ASSOCSTR_DDETOPIC","shlwapi/ASSOCSTR_DEFAULTICON","shlwapi/ASSOCSTR_DELEGATEEXECUTE","shlwapi/ASSOCSTR_DROPTARGET","shlwapi/ASSOCSTR_EXECUTABLE","shlwapi/ASSOCSTR_FRIENDLYAPPNAME","shlwapi/ASSOCSTR_FRIENDLYDOCNAME","shlwapi/ASSOCSTR_INFOTIP","shlwapi/ASSOCSTR_MAX","shlwapi/ASSOCSTR_NOOPEN","shlwapi/ASSOCSTR_PROGID","shlwapi/ASSOCSTR_QUICKTIP","shlwapi/ASSOCSTR_SHELLEXTENSION","shlwapi/ASSOCSTR_SHELLNEWVALUE","shlwapi/ASSOCSTR_SUPPORTED_URI_PROTOCOLS","shlwapi/ASSOCSTR_TILEINFO"]
old-location: shell\ASSOCSTR_str.htm
tech.root: shell
ms.assetid: b5fd3d25-3630-4dd8-acd2-d2e4ed571604
ms.date: 12/05/2018
ms.keywords: ASSOCSTR, ASSOCSTR enumeration [Windows Shell], ASSOCSTR_APPICONREFERENCE, ASSOCSTR_APPID, ASSOCSTR_APPPUBLISHER, ASSOCSTR_COMMAND, ASSOCSTR_CONTENTTYPE, ASSOCSTR_DDEAPPLICATION, ASSOCSTR_DDECOMMAND, ASSOCSTR_DDEIFEXEC, ASSOCSTR_DDETOPIC, ASSOCSTR_DEFAULTICON, ASSOCSTR_DELEGATEEXECUTE, ASSOCSTR_DROPTARGET, ASSOCSTR_EXECUTABLE, ASSOCSTR_FRIENDLYAPPNAME, ASSOCSTR_FRIENDLYDOCNAME, ASSOCSTR_INFOTIP, ASSOCSTR_MAX, ASSOCSTR_NOOPEN, ASSOCSTR_PROGID, ASSOCSTR_QUICKTIP, ASSOCSTR_SHELLEXTENSION, ASSOCSTR_SHELLNEWVALUE, ASSOCSTR_SUPPORTED_URI_PROTOCOLS, ASSOCSTR_TILEINFO, _win32_ASSOCSTR_str, shell.ASSOCSTR_str, shlwapi/ASSOCSTR, shlwapi/ASSOCSTR_APPICONREFERENCE, shlwapi/ASSOCSTR_APPID, shlwapi/ASSOCSTR_APPPUBLISHER, shlwapi/ASSOCSTR_COMMAND, shlwapi/ASSOCSTR_CONTENTTYPE, shlwapi/ASSOCSTR_DDEAPPLICATION, shlwapi/ASSOCSTR_DDECOMMAND, shlwapi/ASSOCSTR_DDEIFEXEC, shlwapi/ASSOCSTR_DDETOPIC, shlwapi/ASSOCSTR_DEFAULTICON, shlwapi/ASSOCSTR_DELEGATEEXECUTE, shlwapi/ASSOCSTR_DROPTARGET, shlwapi/ASSOCSTR_EXECUTABLE, shlwapi/ASSOCSTR_FRIENDLYAPPNAME, shlwapi/ASSOCSTR_FRIENDLYDOCNAME, shlwapi/ASSOCSTR_INFOTIP, shlwapi/ASSOCSTR_MAX, shlwapi/ASSOCSTR_NOOPEN, shlwapi/ASSOCSTR_PROGID, shlwapi/ASSOCSTR_QUICKTIP, shlwapi/ASSOCSTR_SHELLEXTENSION, shlwapi/ASSOCSTR_SHELLNEWVALUE, shlwapi/ASSOCSTR_SUPPORTED_URI_PROTOCOLS, shlwapi/ASSOCSTR_TILEINFO
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP, Windows 7 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ASSOCSTR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ASSOCSTR
 - shlwapi/ASSOCSTR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - ASSOCSTR
---

# ASSOCSTR enumeration


## -description

Used by <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getstring">IQueryAssociations::GetString</a> to define the type of string that is to be returned.

## -enum-fields

### -field ASSOCSTR_COMMAND:1

A command string associated with a Shell verb.

### -field ASSOCSTR_EXECUTABLE

An executable from a Shell verb command string. For example, this string is found as the (Default) value for a subkey such as 
                    
                        <b>HKEY_CLASSES_ROOT</b>&#92;<i>ApplicationName</i>&#92;<b>shell</b>&#92;<b>Open</b>&#92;<b>command</b>. If the command uses Rundll.exe, set the <b>ASSOCF_REMAPRUNDLL</b> flag in the <i>flags</i> parameter of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getstring">IQueryAssociations::GetString</a> to retrieve the target executable.

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

Corresponds to the InfoTip registry value. Returns an info tip for an item, or list of properties in the form of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a> from which to create an info tip, such as when hovering the cursor over a file name. The list of properties can be parsed with <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescriptionlistfromstring">PSGetPropertyDescriptionListFromString</a>.

### -field ASSOCSTR_QUICKTIP

<b>Introduced in Internet Explorer 6</b>. Corresponds to the QuickTip registry value. Same as ASSOCSTR_INFOTIP, except that it always returns a list of property names in the form of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a>. The difference between this value and ASSOCSTR_INFOTIP is that this returns properties that are safe for any scenario that causes slow property retrieval, such as offline or slow networks. Some of the properties returned from ASSOCSTR_INFOTIP might not be appropriate for slow property retrieval scenarios. The list of properties can be parsed with <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescriptionlistfromstring">PSGetPropertyDescriptionListFromString</a>.

### -field ASSOCSTR_TILEINFO

<b>Introduced in Internet Explorer 6</b>. Corresponds to the TileInfo registry value. Contains a list of properties to be displayed for a particular file type in a Windows Explorer window that is in tile view. This is the same as ASSOCSTR_INFOTIP, but, like ASSOCSTR_QUICKTIP, it also returns a list of property names in the form of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a>. The list of properties can be parsed with <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescriptionlistfromstring">PSGetPropertyDescriptionListFromString</a>.

### -field ASSOCSTR_CONTENTTYPE

<b>Introduced in Internet Explorer 6</b>. Describes a general type of MIME file association, such as image and bmp, so that applications can make general assumptions about a specific file type.

### -field ASSOCSTR_DEFAULTICON

<b>Introduced in Internet Explorer 6</b>. Returns the path to the icon resources to use by default for this association. Positive numbers indicate an index into the dll's resource table, while negative numbers indicate a resource ID. An example of the syntax for the resource is "c:\myfolder\myfile.dll,-1".

### -field ASSOCSTR_SHELLEXTENSION

<b>Introduced in Internet Explorer 6</b>. For an object that has a Shell extension associated with it, you can use this to retrieve the CLSID of that Shell extension object by passing a string representation of the IID of the interface you want to retrieve as the <i>pwszExtra</i> parameter of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getstring">IQueryAssociations::GetString</a>. For example, if you want to retrieve a handler that implements the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage">IExtractImage</a> interface, you would specify "{BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}", which is the IID of <b>IExtractImage</b>.

### -field ASSOCSTR_DROPTARGET

<b>Introduced in Internet Explorer 8</b>. For a verb invoked through COM and the <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface, you can use this flag to retrieve the <b>IDropTarget</b> object's CLSID. This CLSID is registered in the <b>DropTarget</b> subkey. The verb is specified in the <i>pwszExtra</i> parameter in the call to <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getstring">IQueryAssociations::GetString</a>.

This type of string will identify the code that will be invoked in the implementation of the verb.

### -field ASSOCSTR_DELEGATEEXECUTE

<b>Introduced in Internet Explorer 8</b>. For a verb invoked through COM and the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand">IExecuteCommand</a> interface, you can use this flag to retrieve the <b>IExecuteCommand</b> object's CLSID. This CLSID is registered in the verb's <b>command</b> subkey as the DelegateExecute entry. The verb is specified in the <i>pwszExtra</i> parameter in the call to <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getstring">IQueryAssociations::GetString</a>.

This type of string will identify the code that will be invoked in the implementation of the verb.

### -field ASSOCSTR_SUPPORTED_URI_PROTOCOLS

A string value of the URI protocol schemes. For example, `http:https:ftp:file:` or `*` indicating all.

### -field ASSOCSTR_PROGID

<b>Introduced in Windows 10</b>. The ProgID provided by the app associated with the file type or URI scheme. This if configured by users in their default program settings.

### -field ASSOCSTR_APPID

<b>Introduced in Windows 10</b>. The AppUserModelID of the app associated with the file type or URI scheme. This is configured by users in their default program settings.

### -field ASSOCSTR_APPPUBLISHER

<b>Introduced in Windows 10</b>. The publisher of the app associated with the file type or URI scheme. This is configured by users in their default program settings.

### -field ASSOCSTR_APPICONREFERENCE

<b>Introduced in Windows 10</b>. The icon reference of the app associated with the file type or URI scheme. This is configured by users in their default program settings.

### -field ASSOCSTR_MAX

The maximum defined ASSOCSTR value, used for validation purposes.
