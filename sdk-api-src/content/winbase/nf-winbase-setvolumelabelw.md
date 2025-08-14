---
UID: NF:winbase.SetVolumeLabelW
title: SetVolumeLabelW function (winbase.h)
description: Sets the label of a file system volume. (Unicode)
helpviewer_keywords: ["SetVolumeLabel", "SetVolumeLabel function [Files]", "SetVolumeLabelW", "_win32_setvolumelabel", "base.setvolumelabel", "fs.setvolumelabel", "winbase/SetVolumeLabel", "winbase/SetVolumeLabelW"]
old-location: fs\setvolumelabel.htm
tech.root: fs
ms.assetid: 1851ed79-7a29-4731-8b67-75d6e9220705
ms.date: 12/05/2018
ms.keywords: SetVolumeLabel, SetVolumeLabel function [Files], SetVolumeLabelA, SetVolumeLabelW, _win32_setvolumelabel, base.setvolumelabel, fs.setvolumelabel, winbase/SetVolumeLabel, winbase/SetVolumeLabelA, winbase/SetVolumeLabelW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetVolumeLabelW (Unicode) and SetVolumeLabelA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetVolumeLabelW
 - winbase/SetVolumeLabelW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - SetVolumeLabel
 - SetVolumeLabelA
 - SetVolumeLabelW
---

# SetVolumeLabelW function


## -description

Sets the label of a file system volume.

## -parameters

### -param lpRootPathName [in, optional]

A pointer to a string that contains the volume's drive letter (for example, X:\) or the path 
      of a mounted folder that is associated with the volume (for example, Y:\MountX\). The string must 
      end with a trailing backslash ('\'). If this parameter is <b>NULL</b>, the root of the 
      current directory is used.

### -param lpVolumeName [in, optional]

A pointer to a string that contains the new label for the volume. If this parameter is 
      <b>NULL</b>, the function deletes any existing label from the specified volume and does not 
      assign a new label.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The maximum volume label length is 32 characters.

<b>FAT filesystems:  </b>The maximum volume label length is 11 characters.

A label is a user-friendly name that a user assigns to a volume to make it easier to recognize. A volume can 
    have a label, a drive letter, both, or neither. For more information, see 
    <a href="/windows/desktop/FileIO/naming-a-volume">Naming a Volume</a>.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 

SMB does not support volume management functions.





> [!NOTE]
> The winbase.h header defines SetVolumeLabel as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa">GetVolumeInformation</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
