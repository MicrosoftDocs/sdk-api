---
UID: NS:wsbonline._WSB_OB_STATUS_ENTRY
title: WSB_OB_STATUS_ENTRY (wsbonline.h)
description: Contains status information for one entry to be shown in the Windows Server Backup MMC snap-in.
helpviewer_keywords: ["WSB_OB_STATUS_ENTRY","WSB_OB_STATUS_ENTRY structure [Windows Server Backup]","wsb.wsb_ob_status_entry","wsbonline/WSB_OB_STATUS_ENTRY"]
old-location: wsb\wsb_ob_status_entry.htm
tech.root: wsb
ms.assetid: BFC13B54-60F3-43A1-B464-D09DD96F57FA
ms.date: 12/05/2018
ms.keywords: WSB_OB_STATUS_ENTRY, WSB_OB_STATUS_ENTRY structure [Windows Server Backup], wsb.wsb_ob_status_entry, wsbonline/WSB_OB_STATUS_ENTRY
req.header: wsbonline.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.typenames: WSB_OB_STATUS_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSB_OB_STATUS_ENTRY
 - wsbonline/_WSB_OB_STATUS_ENTRY
 - WSB_OB_STATUS_ENTRY
 - wsbonline/WSB_OB_STATUS_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsbOnline.h
api_name:
 - WSB_OB_STATUS_ENTRY
---

# WSB_OB_STATUS_ENTRY structure


## -description

 The <b>WSB_OB_STATUS_ENTRY</b> structure contains status 
    information for one entry to be shown in the Windows Server Backup MMC snap-in.

## -struct-fields

### -field m_dwIcon

The resource identifier of the icon to be shown with the status entry. A value of zero indicates no icon is 
      to be shown.

### -field m_dwStatusEntryName

The resource identifier of the name of the status entry.

### -field m_dwStatusEntryValue

The resource identifier of the value of the status entry.

### -field m_cValueTypePair

The number of 
      <a href="/windows/win32/api/wsbonline/ns-wsbonline-wsb_ob_status_entry_value_type_pair">WSB_OB_STATUS_ENTRY_VALUE_TYPE_PAIR</a> 
      structures pointed to by the <b>m_rgValueTypePair</b> member.

### -field m_rgValueTypePair

The list of parameters used to expand the value string contained in the 
      <b>m_dwStatusEntryValue</b> member.

## -remarks

The resources indicated by the resource IDs contained in the <b>m_dwIcon</b>, 
      <b>m_dwStatusEntryName</b> and <b>m_dwStatusEntryValue</b> members will 
      be loaded from the same DLL provided by the cloud backup provider during its registration with Windows Server 
      Backup. For example, an entry name resource ID could point to the string "Total Backups:" or an 
      entry value resource ID could point to the string "%0 copies".

## -see-also

<a href="/previous-versions/windows/desktop/wsb/windows-server-backup-api-structures">Cloud  Backup Provider API Structures</a>



<a href="/windows/win32/api/wsbonline/ns-wsbonline-wsb_ob_status_entry_value_type_pair">WSB_OB_STATUS_ENTRY_VALUE_TYPE_PAIR</a>