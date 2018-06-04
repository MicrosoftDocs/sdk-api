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

# TAG macro


## -description


Identifies an entry in the shim database.


The following entries are of type <b>TAG_TYPE_LIST</b> (0x7000).


<table>
<tr>
<th>Constant/value</th>
<th>Description</th>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_DATABASE"></a><a id="tag_database"></a><dl>
<dt><b>TAG_DATABASE</b></dt>
<dt>(0x1 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Database entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_LIBRARY"></a><a id="tag_library"></a><dl>
<dt><b>TAG_LIBRARY</b></dt>
<dt>(0x2 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Library entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_INEXCLUDE"></a><a id="tag_inexclude"></a><dl>
<dt><b>TAG_INEXCLUDE</b></dt>
<dt>(0x3 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Include and exclude entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_SHIM"></a><a id="tag_shim"></a><dl>
<dt><b>TAG_SHIM</b></dt>
<dt>(0x4 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Shim entry that contains the name and purpose information.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_PATCH"></a><a id="tag_patch"></a><dl>
<dt><b>TAG_PATCH</b></dt>
<dt>(0x5 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Patch entry that contains the in-memory patching information.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_APP"></a><a id="tag_app"></a><dl>
<dt><b>TAG_APP</b></dt>
<dt>(0x6 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Application entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_EXE"></a><a id="tag_exe"></a><dl>
<dt><b>TAG_EXE</b></dt>
<dt>(0x7 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Executable entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MATCHING_FILE"></a><a id="tag_matching_file"></a><dl>
<dt><b>TAG_MATCHING_FILE</b></dt>
<dt>(0x8 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Matching file entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_SHIM_REF"></a><a id="tag_shim_ref"></a><dl>
<dt><b>TAG_SHIM_REF</b></dt>
<dt>(0x9| TAG_TYPE_LIST)</dt>
</dl>
</td>
<td align="left" width="60%">
Shim definition entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_PATCH_REF"></a><a id="tag_patch_ref"></a><dl>
<dt><b>TAG_PATCH_REF</b></dt>
<dt>(0xA | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Patch definition entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_LAYER"></a><a id="tag_layer"></a><dl>
<dt><b>TAG_LAYER</b></dt>
<dt>(0xB | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Layer shim entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FILE"></a><a id="tag_file"></a><dl>
<dt><b>TAG_FILE</b></dt>
<dt>(0xC | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
File attribute used in a shim entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_APPHELP"></a><a id="tag_apphelp"></a><dl>
<dt><b>TAG_APPHELP</b></dt>
<dt>(0xD | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Apphelp information entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_LINK"></a><a id="tag_link"></a><dl>
<dt><b>TAG_LINK</b></dt>
<dt>(0xE | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Apphelp online link information entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_DATA"></a><a id="tag_data"></a><dl>
<dt><b>TAG_DATA</b></dt>
<dt>(0xF | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Name-value mapping entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MSI_TRANSFORM"></a><a id="tag_msi_transform"></a><dl>
<dt><b>TAG_MSI_TRANSFORM</b></dt>
<dt>(0x10 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
MSI transformation entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MSI_TRANSFORM_REF"></a><a id="tag_msi_transform_ref"></a><dl>
<dt><b>TAG_MSI_TRANSFORM_REF</b></dt>
<dt>(0x11 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
MSI transformation definition entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MSI_PACKAGE"></a><a id="tag_msi_package"></a><dl>
<dt><b>TAG_MSI_PACKAGE</b></dt>
<dt>(0x12 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
MSI package entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAG"></a><a id="tag_flag"></a><dl>
<dt><b>TAG_FLAG</b></dt>
<dt>(0x13 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Flag entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MSI_CUSTOM_ACTION"></a><a id="tag_msi_custom_action"></a><dl>
<dt><b>TAG_MSI_CUSTOM_ACTION</b></dt>
<dt>(0x14 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
MSI custom action entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAG_REF"></a><a id="tag_flag_ref"></a><dl>
<dt><b>TAG_FLAG_REF</b></dt>
<dt>(0x15 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Flag definition entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_ACTION"></a><a id="tag_action"></a><dl>
<dt><b>TAG_ACTION</b></dt>
<dt>(0x16 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Unused.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_LOOKUP"></a><a id="tag_lookup"></a><dl>
<dt><b>TAG_LOOKUP</b></dt>
<dt>(0x17 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Lookup entry used for lookup in a driver database.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_STRINGTABLE"></a><a id="tag_stringtable"></a><dl>
<dt><b>TAG_STRINGTABLE</b></dt>
<dt>(0x801 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
String table entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_INDEXES"></a><a id="tag_indexes"></a><dl>
<dt><b>TAG_INDEXES</b></dt>
<dt>(0x802 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Indexes entry that defines all the indexes in a shim database.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_INDEX"></a><a id="tag_index"></a><dl>
<dt><b>TAG_INDEX</b></dt>
<dt>(0x803 | <b>TAG_TYPE_LIST</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Index entry that defines an index in a shim database.

</td>
</tr>
</table>
The following entries are of type <b>TAG_TYPE_STRINGREF</b> (0x6000).


<table>
<tr>
<th>Constant/value</th>
<th>Description</th>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_NAME"></a><a id="tag_name"></a><dl>
<dt><b>TAG_NAME</b></dt>
<dt>(0x1 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Name attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_DESCRIPTION"></a><a id="tag_description"></a><dl>
<dt><b>TAG_DESCRIPTION</b></dt>
<dt>(0x2 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Description entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MODULE"></a><a id="tag_module"></a><dl>
<dt><b>TAG_MODULE</b></dt>
<dt>(0x3 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Module attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_API"></a><a id="tag_api"></a><dl>
<dt><b>TAG_API</b></dt>
<dt>(0x4 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
API entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_VENDOR"></a><a id="tag_vendor"></a><dl>
<dt><b>TAG_VENDOR</b></dt>
<dt>(0x5 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Vendor name attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_APP_NAME"></a><a id="tag_app_name"></a><dl>
<dt><b>TAG_APP_NAME</b></dt>
<dt>(0x6 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Application name attribute that describes an application entry in a shim database.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_COMMAND_LINE"></a><a id="tag_command_line"></a><dl>
<dt><b>TAG_COMMAND_LINE</b></dt>
<dt>(0x8 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Command line attribute that is used when passing arguments to a shim, for example.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_COMPANY_NAME"></a><a id="tag_company_name"></a><dl>
<dt><b>TAG_COMPANY_NAME</b></dt>
<dt>(0x9 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Company name attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_DLLFILE"></a><a id="tag_dllfile"></a><dl>
<dt><b>TAG_DLLFILE</b></dt>
<dt>(0xA | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
DLL file attribute for a shim entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_WILDCARD_NAME"></a><a id="tag_wildcard_name"></a><dl>
<dt><b>TAG_WILDCARD_NAME</b></dt>
<dt>(0xB | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Wildcard name attribute for an executable entry with a wildcard as the file name.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_PRODUCT_NAME"></a><a id="tag_product_name"></a><dl>
<dt><b>TAG_PRODUCT_NAME</b></dt>
<dt>(0x10 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Product name attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_PRODUCT_VERSION"></a><a id="tag_product_version"></a><dl>
<dt><b>TAG_PRODUCT_VERSION</b></dt>
<dt>(0x11 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Product version attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FILE_DESCRIPTION"></a><a id="tag_file_description"></a><dl>
<dt><b>TAG_FILE_DESCRIPTION</b></dt>
<dt>(0x12 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
File description attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FILE_VERSION"></a><a id="tag_file_version"></a><dl>
<dt><b>TAG_FILE_VERSION</b></dt>
<dt>(0x13 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
File version attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_ORIGINAL_FILENAME"></a><a id="tag_original_filename"></a><dl>
<dt><b>TAG_ORIGINAL_FILENAME</b></dt>
<dt>(0x14 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Original file name attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_INTERNAL_NAME"></a><a id="tag_internal_name"></a><dl>
<dt><b>TAG_INTERNAL_NAME</b></dt>
<dt>(0x15 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Internal file name attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_LEGAL_COPYRIGHT"></a><a id="tag_legal_copyright"></a><dl>
<dt><b>TAG_LEGAL_COPYRIGHT</b></dt>
<dt>(0x16 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Copyright attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_16BIT_DESCRIPTION"></a><a id="tag_16bit_description"></a><dl>
<dt><b>TAG_16BIT_DESCRIPTION</b></dt>
<dt>(0x17 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
16-bit description attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_APPHELP_DETAILS"></a><a id="tag_apphelp_details"></a><dl>
<dt><b>TAG_APPHELP_DETAILS</b></dt>
<dt>(0x18 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Apphelp details message information attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_LINK_URL"></a><a id="tag_link_url"></a><dl>
<dt><b>TAG_LINK_URL</b></dt>
<dt>(0x19 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Apphelp online link URL attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_LINK_TEXT"></a><a id="tag_link_text"></a><dl>
<dt><b>TAG_LINK_TEXT</b></dt>
<dt>(0x1A | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Apphelp online link text attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_APPHELP_TITLE"></a><a id="tag_apphelp_title"></a><dl>
<dt><b>TAG_APPHELP_TITLE</b></dt>
<dt>(0x1B | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Apphelp title attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_APPHELP_CONTACT"></a><a id="tag_apphelp_contact"></a><dl>
<dt><b>TAG_APPHELP_CONTACT</b></dt>
<dt>(0x1C | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Apphelp vendor contact attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_SXS_MANIFEST"></a><a id="tag_sxs_manifest"></a><dl>
<dt><b>TAG_SXS_MANIFEST</b></dt>
<dt>(0x1D | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Side-by-side manifest entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_DATA_STRING"></a><a id="tag_data_string"></a><dl>
<dt><b>TAG_DATA_STRING</b></dt>
<dt>(0x1E | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
String attribute for a data entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MSI_TRANSFORM_FILE"></a><a id="tag_msi_transform_file"></a><dl>
<dt><b>TAG_MSI_TRANSFORM_FILE</b></dt>
<dt>(0x1F | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
File name attribute of an MSI transformation entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_16BIT_MODULE_NAME"></a><a id="tag_16bit_module_name"></a><dl>
<dt><b>TAG_16BIT_MODULE_NAME</b></dt>
<dt>(0x20 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
16-bit module name attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_LAYER_DISPLAYNAME"></a><a id="tag_layer_displayname"></a><dl>
<dt><b>TAG_LAYER_DISPLAYNAME</b></dt>
<dt>(0x21 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Unused.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_COMPILER_VERSION"></a><a id="tag_compiler_version"></a><dl>
<dt><b>TAG_COMPILER_VERSION</b></dt>
<dt>(0x22 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Shim database compiler version.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_ACTION_TYPE"></a><a id="tag_action_type"></a><dl>
<dt><b>TAG_ACTION_TYPE</b></dt>
<dt>(0x23 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Unused.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_EXPORT_NAME"></a><a id="tag_export_name"></a><dl>
<dt><b>TAG_EXPORT_NAME</b></dt>
<dt>(0x24 | <b>TAG_TYPE_STRINGREF</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Export file name attribute.

</td>
</tr>
</table>
The following entries are of type <b>TAG_TYPE_DWORD</b> (0x4000).


<table>
<tr>
<th>Constant/value</th>
<th>Description</th>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_SIZE"></a><a id="tag_size"></a><dl>
<dt><b>TAG_SIZE</b></dt>
<dt>(0x1 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
File size attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_OFFSET"></a><a id="tag_offset"></a><dl>
<dt><b>TAG_OFFSET</b></dt>
<dt>(0x2 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Unused.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_CHECKSUM"></a><a id="tag_checksum"></a><dl>
<dt><b>TAG_CHECKSUM</b></dt>
<dt>(0x3 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
File checksum attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_SHIM_TAGID"></a><a id="tag_shim_tagid"></a><dl>
<dt><b>TAG_SHIM_TAGID</b></dt>
<dt>(0x4 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Shim <b>TAGID</b> attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_PATCH_TAGID"></a><a id="tag_patch_tagid"></a><dl>
<dt><b>TAG_PATCH_TAGID</b></dt>
<dt>(0x5 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Patch <b>TAGID</b> attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MODULE_TYPE"></a><a id="tag_module_type"></a><dl>
<dt><b>TAG_MODULE_TYPE</b></dt>
<dt>(0x6 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Module type attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_VERDATEHI"></a><a id="tag_verdatehi"></a><dl>
<dt><b>TAG_VERDATEHI</b></dt>
<dt>(0x7 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
High-order portion of the file version date attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_VERDATELO"></a><a id="tag_verdatelo"></a><dl>
<dt><b>TAG_VERDATELO</b></dt>
<dt>(0x8 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Low-order portion of the file version date attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_VERFILEOS"></a><a id="tag_verfileos"></a><dl>
<dt><b>TAG_VERFILEOS</b></dt>
<dt>(0x9 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Operating system file version attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_VERFILETYPE"></a><a id="tag_verfiletype"></a><dl>
<dt><b>TAG_VERFILETYPE</b></dt>
<dt>(0xA | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
File type attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_PE_CHECKSUM"></a><a id="tag_pe_checksum"></a><dl>
<dt><b>TAG_PE_CHECKSUM</b></dt>
<dt>(0xB | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
PE file checksum attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_PREVOSMAJORVER"></a><a id="tag_prevosmajorver"></a><dl>
<dt><b>TAG_PREVOSMAJORVER</b></dt>
<dt>(0xC | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Major operating system version attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_PREVOSMINORVER"></a><a id="tag_prevosminorver"></a><dl>
<dt><b>TAG_PREVOSMINORVER</b></dt>
<dt>(0xD | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Minor operating system version attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_PREVOSPLATFORMID"></a><a id="tag_prevosplatformid"></a><dl>
<dt><b>TAG_PREVOSPLATFORMID</b></dt>
<dt>(0xE | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Operating system platform identifier attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_PREVOSBUILDNO"></a><a id="tag_prevosbuildno"></a><dl>
<dt><b>TAG_PREVOSBUILDNO</b></dt>
<dt>(0xF | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Operating system build number attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_PROBLEMSEVERITY"></a><a id="tag_problemseverity"></a><dl>
<dt><b>TAG_PROBLEMSEVERITY</b></dt>
<dt>(0x10 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Block attribute of an Apphelp entry. This determines whether the application is hard or soft blocked.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_LANGID"></a><a id="tag_langid"></a><dl>
<dt><b>TAG_LANGID</b></dt>
<dt>(0x11 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Language identifier of an Apphelp entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_VER_LANGUAGE"></a><a id="tag_ver_language"></a><dl>
<dt><b>TAG_VER_LANGUAGE</b></dt>
<dt>(0x12 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Language version attribute of a file.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_ENGINE"></a><a id="tag_engine"></a><dl>
<dt><b>TAG_ENGINE</b></dt>
<dt>(0x14 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Unused.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_HTMLHELPID"></a><a id="tag_htmlhelpid"></a><dl>
<dt><b>TAG_HTMLHELPID</b></dt>
<dt>(0x15 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Help identifier attribute for an Apphelp entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_INDEX_FLAGS"></a><a id="tag_index_flags"></a><dl>
<dt><b>TAG_INDEX_FLAGS</b></dt>
<dt>(0x16 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Flags attribute for an index entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAGS"></a><a id="tag_flags"></a><dl>
<dt><b>TAG_FLAGS</b></dt>
<dt>(0x17 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Flags attribute for an Apphelp entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_DATA_VALUETYPE"></a><a id="tag_data_valuetype"></a><dl>
<dt><b>TAG_DATA_VALUETYPE</b></dt>
<dt>(0x18 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Data type attribute for a data entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_DATA_DWORD"></a><a id="tag_data_dword"></a><dl>
<dt><b>TAG_DATA_DWORD</b></dt>
<dt>(0x19 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
<b>DWORD</b> value attribute for a data entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_LAYER_TAGID"></a><a id="tag_layer_tagid"></a><dl>
<dt><b>TAG_LAYER_TAGID</b></dt>
<dt>(0x1A | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Layer shim <b>TAGID</b> attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MSI_TRANSFORM_TAGID"></a><a id="tag_msi_transform_tagid"></a><dl>
<dt><b>TAG_MSI_TRANSFORM_TAGID</b></dt>
<dt>(0x1B | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
MSI transform <b>TAGID</b> attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_LINKER_VERSION"></a><a id="tag_linker_version"></a><dl>
<dt><b>TAG_LINKER_VERSION</b></dt>
<dt>(0x1C | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Linker version attribute of a file.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_LINK_DATE"></a><a id="tag_link_date"></a><dl>
<dt><b>TAG_LINK_DATE</b></dt>
<dt>(0x1D | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Link date attribute of a file.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_UPTO_LINK_DATE"></a><a id="tag_upto_link_date"></a><dl>
<dt><b>TAG_UPTO_LINK_DATE</b></dt>
<dt>(0x1E | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Link date attribute of a file. Matching is done up to and including this link date.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_OS_SERVICE_PACK"></a><a id="tag_os_service_pack"></a><dl>
<dt><b>TAG_OS_SERVICE_PACK</b></dt>
<dt>(0x1F | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Operating system service pack attribute for an executable entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAG_TAGID"></a><a id="tag_flag_tagid"></a><dl>
<dt><b>TAG_FLAG_TAGID</b></dt>
<dt>(0x20 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Flags <b>TAGID</b> attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_RUNTIME_PLATFORM"></a><a id="tag_runtime_platform"></a><dl>
<dt><b>TAG_RUNTIME_PLATFORM</b></dt>
<dt>(0x21 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Run-time platform attribute of a file.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_OS_SKU"></a><a id="tag_os_sku"></a><dl>
<dt><b>TAG_OS_SKU</b></dt>
<dt>(0x22 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Operating system SKU attribute for an executable entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_OS_PLATFORM"></a><a id="tag_os_platform"></a><dl>
<dt><b>TAG_OS_PLATFORM</b></dt>
<dt>(0x23 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Operating system platform attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_APP_NAME_RC_ID"></a><a id="tag_app_name_rc_id"></a><dl>
<dt><b>TAG_APP_NAME_RC_ID</b></dt>
<dt>(0x24 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Application name resource identifier attribute for Apphelp entries.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_VENDOR_NAME_RC_ID"></a><a id="tag_vendor_name_rc_id"></a><dl>
<dt><b>TAG_VENDOR_NAME_RC_ID</b></dt>
<dt>(0x25 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Vendor name resource identifier attribute for Apphelp entries.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_SUMMARY_MSG_RC_ID"></a><a id="tag_summary_msg_rc_id"></a><dl>
<dt><b>TAG_SUMMARY_MSG_RC_ID</b></dt>
<dt>(0x26 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Summary message resource identifier attribute for Apphelp entries.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_VISTA_SKU"></a><a id="tag_vista_sku"></a><dl>
<dt><b>TAG_VISTA_SKU</b></dt>
<dt>(0x27 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Windows Vista SKU attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_DESCRIPTION_RC_ID"></a><a id="tag_description_rc_id"></a><dl>
<dt><b>TAG_DESCRIPTION_RC_ID</b></dt>
<dt>(0x28 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Description resource identifier attribute for Apphelp entries.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_PARAMETER1_RC_ID"></a><a id="tag_parameter1_rc_id"></a><dl>
<dt><b>TAG_PARAMETER1_RC_ID</b></dt>
<dt>(0x29 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Parameter1 resource identifier attribute for Apphelp entries.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_TAGID"></a><a id="tag_tagid"></a><dl>
<dt><b>TAG_TAGID</b></dt>
<dt>(0x801 | <b>TAG_TYPE_DWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
<b>TAGID</b> attribute.

</td>
</tr>
</table>
The following entry is of type <b>TAG_TYPE_STRING</b> (0x8000).


<table>
<tr>
<th>Constant/value</th>
<th>Description</th>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_STRINGTABLE_ITEM"></a><a id="tag_stringtable_item"></a><dl>
<dt><b>TAG_STRINGTABLE_ITEM</b></dt>
<dt>(0x801 | <b>TAG_TYPE_STRING</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
String table item entry.

</td>
</tr>
</table>
The following entries are of type <b>TAG_TYPE_NULL</b> (0x1000).


<table>
<tr>
<th>Constant/value</th>
<th>Description</th>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_INCLUDE"></a><a id="tag_include"></a><dl>
<dt><b>TAG_INCLUDE</b></dt>
<dt>(0x1 | <b>TAG_TYPE_NULL</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Include list entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_GENERAL"></a><a id="tag_general"></a><dl>
<dt><b>TAG_GENERAL</b></dt>
<dt>(0x2 | <b>TAG_TYPE_NULL</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
General purpose shim entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MATCH_LOGIC_NOT"></a><a id="tag_match_logic_not"></a><dl>
<dt><b>TAG_MATCH_LOGIC_NOT</b></dt>
<dt>(0x3 | <b>TAG_TYPE_NULL</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
NOT of matching logic entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_APPLY_ALL_SHIMS"></a><a id="tag_apply_all_shims"></a><dl>
<dt><b>TAG_APPLY_ALL_SHIMS</b></dt>
<dt>(0x4 | <b>TAG_TYPE_NULL</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Unused.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_USE_SERVICE_PACK_FILES"></a><a id="tag_use_service_pack_files"></a><dl>
<dt><b>TAG_USE_SERVICE_PACK_FILES</b></dt>
<dt>(0x5 | <b>TAG_TYPE_NULL</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Service pack information for Apphelp entries.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MITIGATION_OS"></a><a id="tag_mitigation_os"></a><dl>
<dt><b>TAG_MITIGATION_OS</b></dt>
<dt>(0x6 | <b>TAG_TYPE_NULL</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Mitigation at operating system scope entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_BLOCK_UPGRADE"></a><a id="tag_block_upgrade"></a><dl>
<dt><b>TAG_BLOCK_UPGRADE</b></dt>
<dt>(0x7 | <b>TAG_TYPE_NULL</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Upgrade block entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_INCLUDEEXCLUDEDLL"></a><a id="tag_includeexcludedll"></a><dl>
<dt><b>TAG_INCLUDEEXCLUDEDLL</b></dt>
<dt>(0x8 | <b>TAG_TYPE_NULL</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
DLL include/exclude entry.

</td>
</tr>
</table>
The following entries are of type <b>TAG_TYPE_QWORD</b> (0x5000).


<table>
<tr>
<th>Constant/value</th>
<th>Description</th>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_TIME"></a><a id="tag_time"></a><dl>
<dt><b>TAG_TIME</b></dt>
<dt>(0x1 | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Time attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_BIN_FILE_VERSION"></a><a id="tag_bin_file_version"></a><dl>
<dt><b>TAG_BIN_FILE_VERSION</b></dt>
<dt>(0x2 | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Bin file version attribute for file entries.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_BIN_PRODUCT_VERSION"></a><a id="tag_bin_product_version"></a><dl>
<dt><b>TAG_BIN_PRODUCT_VERSION</b></dt>
<dt>(0x3 | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Bin product version attribute for file entries.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MODTIME"></a><a id="tag_modtime"></a><dl>
<dt><b>TAG_MODTIME</b></dt>
<dt>(0x4 | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Unused.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAG_MASK_KERNEL"></a><a id="tag_flag_mask_kernel"></a><dl>
<dt><b>TAG_FLAG_MASK_KERNEL</b></dt>
<dt>(0x5 | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Kernel flag mask attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_UPTO_BIN_PRODUCT_VERSION"></a><a id="tag_upto_bin_product_version"></a><dl>
<dt><b>TAG_UPTO_BIN_PRODUCT_VERSION</b></dt>
<dt>(0x6 | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Bin product version attribute of a file. Matching is done up to and including this product version.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_DATA_QWORD"></a><a id="tag_data_qword"></a><dl>
<dt><b>TAG_DATA_QWORD</b></dt>
<dt>(0x7 | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
<b>ULONGLONG</b> value attribute for  a data entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAG_MASK_USER"></a><a id="tag_flag_mask_user"></a><dl>
<dt><b>TAG_FLAG_MASK_USER</b></dt>
<dt>(0x8 | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
User flag mask attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAGS_NTVDM1"></a><a id="tag_flags_ntvdm1"></a><dl>
<dt><b>TAG_FLAGS_NTVDM1</b></dt>
<dt>(0x9 | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
NTVDM1 flag mask attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAGS_NTVDM2"></a><a id="tag_flags_ntvdm2"></a><dl>
<dt><b>TAG_FLAGS_NTVDM2</b></dt>
<dt>(0xA | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
NTVDM2 flag mask attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAGS_NTVDM3"></a><a id="tag_flags_ntvdm3"></a><dl>
<dt><b>TAG_FLAGS_NTVDM3</b></dt>
<dt>(0xB | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
NTVDM3 flag mask attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAG_MASK_SHELL"></a><a id="tag_flag_mask_shell"></a><dl>
<dt><b>TAG_FLAG_MASK_SHELL</b></dt>
<dt>(0xC | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Shell flag mask attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_UPTO_BIN_FILE_VERSION"></a><a id="tag_upto_bin_file_version"></a><dl>
<dt><b>TAG_UPTO_BIN_FILE_VERSION</b></dt>
<dt>(0xD | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Bin file version attribute of a file. Matching is done up to and including this file version.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAG_MASK_FUSION"></a><a id="tag_flag_mask_fusion"></a><dl>
<dt><b>TAG_FLAG_MASK_FUSION</b></dt>
<dt>(0xE | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Fusion flag mask attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAG_PROCESSPARAM"></a><a id="tag_flag_processparam"></a><dl>
<dt><b>TAG_FLAG_PROCESSPARAM</b></dt>
<dt>(0xF | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Process param flag attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAG_LUA"></a><a id="tag_flag_lua"></a><dl>
<dt><b>TAG_FLAG_LUA</b></dt>
<dt>(0x10 | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
LUA flag attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FLAG_INSTALL"></a><a id="tag_flag_install"></a><dl>
<dt><b>TAG_FLAG_INSTALL</b></dt>
<dt>(0x11 | <b>TAG_TYPE_QWORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Install flag attribute.

</td>
</tr>
</table>
The following entries are of type <b>TAG_TYPE_BINARY</b> (0x9000).


<table>
<tr>
<th>Constant/value</th>
<th>Description</th>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_PATCH_BITS"></a><a id="tag_patch_bits"></a><dl>
<dt><b>TAG_PATCH_BITS</b></dt>
<dt>(0x2 | <b>TAG_TYPE_BINARY</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Patch file bits attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_FILE_BITS"></a><a id="tag_file_bits"></a><dl>
<dt><b>TAG_FILE_BITS</b></dt>
<dt>(0x3 | <b>TAG_TYPE_BINARY</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
File bits attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_EXE_ID"></a><a id="tag_exe_id"></a><dl>
<dt><b>TAG_EXE_ID</b></dt>
<dt>(0x4 | <b>TAG_TYPE_BINARY</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
<b>GUID</b> attribute of an executable entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_DATA_BITS"></a><a id="tag_data_bits"></a><dl>
<dt><b>TAG_DATA_BITS</b></dt>
<dt>(0x5 | <b>TAG_TYPE_BINARY</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Data bits attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MSI_PACKAGE_ID"></a><a id="tag_msi_package_id"></a><dl>
<dt><b>TAG_MSI_PACKAGE_ID</b></dt>
<dt>(0x6 | <b>TAG_TYPE_BINARY</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
MSI package identifier attribute of an MSI package.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_DATABASE_ID"></a><a id="tag_database_id"></a><dl>
<dt><b>TAG_DATABASE_ID</b></dt>
<dt>(0x7 | <b>TAG_TYPE_BINARY</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
<b>GUID</b> attribute of a database.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_INDEX_BITS"></a><a id="tag_index_bits"></a><dl>
<dt><b>TAG_INDEX_BITS</b></dt>
<dt>(0x801 | <b>TAG_TYPE_BINARY</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Index bits attribute.

</td>
</tr>
</table>
The following entries are of type <b>TAG_TYPE_WORD</b> (0x3000).


<table>
<tr>
<th>Constant/value</th>
<th>Description</th>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_MATCH_MODE"></a><a id="tag_match_mode"></a><dl>
<dt><b>TAG_MATCH_MODE</b></dt>
<dt>(0x1 | <b>TAG_TYPE_WORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Match mode attribute.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_TAG"></a><a id="tag_tag"></a><dl>
<dt><b>TAG_TAG</b></dt>
<dt>(0x801 | <b>TAG_TYPE_WORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
TAG entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_INDEX_TAG"></a><a id="tag_index_tag"></a><dl>
<dt><b>TAG_INDEX_TAG</b></dt>
<dt>(0x802 | <b>TAG_TYPE_WORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Index TAG attribute for an index entry.

</td>
</tr>
<tr valign="top">
<td align="left" width="40%"><a id="TAG_INDEX_KEY"></a><a id="tag_index_key"></a><dl>
<dt><b>TAG_INDEX_KEY</b></dt>
<dt>(0x803 | <b>TAG_TYPE_WORD</b>)</dt>
</dl>
</td>
<td align="left" width="60%">
Index key attribute for an index entry.

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://msdn.microsoft.com/009ad522-35da-4053-a7f6-61d7d240b98c">TAG Types</a>



<a href="https://msdn.microsoft.com/2ff58e01-cc47-4612-a3bc-a87ccb343bd2">TAGID</a>



<a href="https://msdn.microsoft.com/e7d83dca-13a5-4396-b50b-0d068209c03c">TAGREF</a>
 

 

