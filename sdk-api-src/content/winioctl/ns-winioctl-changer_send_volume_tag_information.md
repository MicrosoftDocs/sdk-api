---
UID: NS:winioctl._CHANGER_SEND_VOLUME_TAG_INFORMATION
title: CHANGER_SEND_VOLUME_TAG_INFORMATION
description: Contains information that the IOCTL_CHANGER_QUERY_VOLUME_TAGS control code uses to determine the volume information to be retrieved.
helpviewer_keywords: ["*PCHANGER_SEND_VOLUME_TAG_INFORMATION","ASSERT_ALTERNATE","ASSERT_PRIMARY","CHANGER_SEND_VOLUME_TAG_INFORMATION","CHANGER_SEND_VOLUME_TAG_INFORMATION structure","PCHANGER_SEND_VOLUME_TAG_INFORMATION","PCHANGER_SEND_VOLUME_TAG_INFORMATION structure pointer","REPLACE_ALTERNATE","REPLACE_PRIMARY","SEARCH_ALL","SEARCH_ALL_NO_SEQ","SEARCH_ALTERNATE","SEARCH_ALT_NO_SEQ","SEARCH_PRIMARY","SEARCH_PRI_NO_SEQ","UNDEFINE_ALTERNATE","UNDEFINE_PRIMARY","_win32_changer_send_volume_tag_information_str","base.changer_send_volume_tag_information_str","winioctl/CHANGER_SEND_VOLUME_TAG_INFORMATION","winioctl/PCHANGER_SEND_VOLUME_TAG_INFORMATION"]
old-location: base\changer_send_volume_tag_information_str.htm
tech.root: base
ms.assetid: 96148983-48be-466d-be7f-c1dbf6910c20
ms.date: 12/05/2018
ms.keywords: '*PCHANGER_SEND_VOLUME_TAG_INFORMATION, ASSERT_ALTERNATE, ASSERT_PRIMARY, CHANGER_SEND_VOLUME_TAG_INFORMATION, CHANGER_SEND_VOLUME_TAG_INFORMATION structure, PCHANGER_SEND_VOLUME_TAG_INFORMATION, PCHANGER_SEND_VOLUME_TAG_INFORMATION structure pointer, REPLACE_ALTERNATE, REPLACE_PRIMARY, SEARCH_ALL, SEARCH_ALL_NO_SEQ, SEARCH_ALTERNATE, SEARCH_ALT_NO_SEQ, SEARCH_PRIMARY, SEARCH_PRI_NO_SEQ, UNDEFINE_ALTERNATE, UNDEFINE_PRIMARY, _win32_changer_send_volume_tag_information_str, base.changer_send_volume_tag_information_str, winioctl/CHANGER_SEND_VOLUME_TAG_INFORMATION, winioctl/PCHANGER_SEND_VOLUME_TAG_INFORMATION'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: CHANGER_SEND_VOLUME_TAG_INFORMATION, *PCHANGER_SEND_VOLUME_TAG_INFORMATION
req.redist: 
f1_keywords:
 - _CHANGER_SEND_VOLUME_TAG_INFORMATION
 - winioctl/_CHANGER_SEND_VOLUME_TAG_INFORMATION
 - PCHANGER_SEND_VOLUME_TAG_INFORMATION
 - winioctl/PCHANGER_SEND_VOLUME_TAG_INFORMATION
 - CHANGER_SEND_VOLUME_TAG_INFORMATION
 - winioctl/CHANGER_SEND_VOLUME_TAG_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - CHANGER_SEND_VOLUME_TAG_INFORMATION
---

# CHANGER_SEND_VOLUME_TAG_INFORMATION structure


## -description

Contains information that the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_query_volume_tags">IOCTL_CHANGER_QUERY_VOLUME_TAGS</a> control code uses to determine the volume information to be retrieved.

## -struct-fields

### -field StartingElement

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a> structure that represents the starting element for which information is to be retrieved.

### -field ActionCode

The action to be performed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ASSERT_ALTERNATE"></a><a id="assert_alternate"></a><dl>
<dt><b>ASSERT_ALTERNATE</b></dt>
<dt>0x9</dt>
</dl>
</td>
<td width="60%">
Define the alternate volume tag of a volume that currently has none defined. 




Requires that <b>Features0</b> is CHANGER_VOLUME_ASSERT.

</td>
</tr>
<tr>
<td width="40%"><a id="ASSERT_PRIMARY"></a><a id="assert_primary"></a><dl>
<dt><b>ASSERT_PRIMARY</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Define the primary volume tag of a volume that currently has none defined. 




Requires that <b>Features0</b> is CHANGER_VOLUME_ASSERT.

</td>
</tr>
<tr>
<td width="40%"><a id="REPLACE_ALTERNATE"></a><a id="replace_alternate"></a><dl>
<dt><b>REPLACE_ALTERNATE</b></dt>
<dt>0xB</dt>
</dl>
</td>
<td width="60%">
Replace the alternate volume tag with a new tag. 




Requires that <b>Features0</b> is CHANGER_VOLUME_REPLACE.

</td>
</tr>
<tr>
<td width="40%"><a id="REPLACE_PRIMARY"></a><a id="replace_primary"></a><dl>
<dt><b>REPLACE_PRIMARY</b></dt>
<dt>0xA</dt>
</dl>
</td>
<td width="60%">
Replace the primary volume tag with a new tag. 




Requires that <b>Features0</b> is CHANGER_VOLUME_REPLACE.

</td>
</tr>
<tr>
<td width="40%"><a id="SEARCH_ALL"></a><a id="search_all"></a><dl>
<dt><b>SEARCH_ALL</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Search all defined volume tags. 




Requires that <b>Features0</b> is CHANGER_VOLUME_SEARCH.

</td>
</tr>
<tr>
<td width="40%"><a id="SEARCH_ALL_NO_SEQ"></a><a id="search_all_no_seq"></a><dl>
<dt><b>SEARCH_ALL_NO_SEQ</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
Search all defined volume tags, but ignore sequence numbers. 




Requires that <b>Features0</b> is CHANGER_VOLUME_SEARCH.

</td>
</tr>
<tr>
<td width="40%"><a id="SEARCH_ALT_NO_SEQ"></a><a id="search_alt_no_seq"></a><dl>
<dt><b>SEARCH_ALT_NO_SEQ</b></dt>
<dt>0x6</dt>
</dl>
</td>
<td width="60%">
Search only alternate volume tags, but ignore sequence numbers. 




Requires that <b>Features0</b> is CHANGER_VOLUME_SEARCH.

</td>
</tr>
<tr>
<td width="40%"><a id="SEARCH_ALTERNATE"></a><a id="search_alternate"></a><dl>
<dt><b>SEARCH_ALTERNATE</b></dt>
<dt>02</dt>
</dl>
</td>
<td width="60%">
Search only alternate volume tags. 




Requires that <b>Features0</b> is CHANGER_VOLUME_SEARCH.

</td>
</tr>
<tr>
<td width="40%"><a id="SEARCH_PRI_NO_SEQ"></a><a id="search_pri_no_seq"></a><dl>
<dt><b>SEARCH_PRI_NO_SEQ</b></dt>
<dt>05</dt>
</dl>
</td>
<td width="60%">
Search only primary volume tags but ignore sequence numbers. 




Requires that <b>Features0</b> is CHANGER_VOLUME_SEARCH.

</td>
</tr>
<tr>
<td width="40%"><a id="SEARCH_PRIMARY"></a><a id="search_primary"></a><dl>
<dt><b>SEARCH_PRIMARY</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Search only primary volume tags. 




Requires that <b>Features0</b> is CHANGER_VOLUME_SEARCH.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDEFINE_ALTERNATE"></a><a id="undefine_alternate"></a><dl>
<dt><b>UNDEFINE_ALTERNATE</b></dt>
<dt>0xD</dt>
</dl>
</td>
<td width="60%">
Clear the alternate volume tag. 




Requires that <b>Features0</b> is CHANGER_VOLUME_UNDEFINE.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDEFINE_PRIMARY"></a><a id="undefine_primary"></a><dl>
<dt><b>UNDEFINE_PRIMARY</b></dt>
<dt>0xC</dt>
</dl>
</td>
<td width="60%">
Clear the primary volume tag. 




Requires that <b>Features0</b> is CHANGER_VOLUME_UNDEFINE.

</td>
</tr>
</table>

### -field VolumeIDTemplate

The template that the device uses to search for volume IDs. For search operations, the template can include wildcard characters to search for volumes that match the template. Supported wildcard characters include the asterisk (*) and question mark (?). For other operations, the template must specify a single volume.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element">CHANGER_ELEMENT</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_query_volume_tags">IOCTL_CHANGER_QUERY_VOLUME_TAGS</a>