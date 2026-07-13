---
UID: NS:winnt._IMAGE_LOAD_CONFIG_DIRECTORY32
title: IMAGE_LOAD_CONFIG_DIRECTORY32 (winnt.h)
description: Contains the load configuration data of an image. (32 bit)
helpviewer_keywords: ["*PIMAGE_LOAD_CONFIG_DIRECTORY32","IMAGE_LOAD_CONFIG_DIRECTORY","IMAGE_LOAD_CONFIG_DIRECTORY32","IMAGE_LOAD_CONFIG_DIRECTORY64","IMAGE_LOAD_CONFIG_DIRECTORY64 structure","PIMAGE_LOAD_CONFIG_DIRECTORY64","PIMAGE_LOAD_CONFIG_DIRECTORY64 structure pointer","_IMAGE_LOAD_CONFIG_DIRECTORY64","base.image_load_config_directory64_str","winnt/IMAGE_LOAD_CONFIG_DIRECTORY64","winnt/PIMAGE_LOAD_CONFIG_DIRECTORY64"]
old-location: base\image_load_config_directory64_str.htm
tech.root: Debug
ms.assetid: ebd42f1a-a5aa-4179-a2d0-61c50469d5c0
ms.date: 12/05/2018
ms.keywords: '*PIMAGE_LOAD_CONFIG_DIRECTORY32, IMAGE_LOAD_CONFIG_DIRECTORY, IMAGE_LOAD_CONFIG_DIRECTORY32, IMAGE_LOAD_CONFIG_DIRECTORY64, IMAGE_LOAD_CONFIG_DIRECTORY64 structure, PIMAGE_LOAD_CONFIG_DIRECTORY64, PIMAGE_LOAD_CONFIG_DIRECTORY64 structure pointer, _IMAGE_LOAD_CONFIG_DIRECTORY64, base.image_load_config_directory64_str, winnt/IMAGE_LOAD_CONFIG_DIRECTORY64, winnt/PIMAGE_LOAD_CONFIG_DIRECTORY64'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: IMAGE_LOAD_CONFIG_DIRECTORY32, *PIMAGE_LOAD_CONFIG_DIRECTORY32
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAGE_LOAD_CONFIG_DIRECTORY32
 - winnt/_IMAGE_LOAD_CONFIG_DIRECTORY32
 - PIMAGE_LOAD_CONFIG_DIRECTORY32
 - winnt/PIMAGE_LOAD_CONFIG_DIRECTORY32
 - IMAGE_LOAD_CONFIG_DIRECTORY32
 - winnt/IMAGE_LOAD_CONFIG_DIRECTORY32
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - IMAGE_LOAD_CONFIG_DIRECTORY64
 - IMAGE_LOAD_CONFIG_DIRECTORY
---

# IMAGE_LOAD_CONFIG_DIRECTORY32 structure


## -description

Contains the load configuration data of an image.

## -struct-fields

### -field Size

The size of the structure. For Windows XP, the size must be specified as 64 for x86 images.

### -field TimeDateStamp

The date and time stamp value. The value is represented in the number of seconds elapsed since midnight (00:00:00), January 1, 1970, Universal Coordinated Time, according to the system clock. The time stamp can be printed using the C run-time (CRT) function <b>ctime</b>.

### -field MajorVersion

The major version number.

### -field MinorVersion

The minor version number.

### -field GlobalFlagsClear

The global flags that control system behavior. For more information, see Gflags.exe.

### -field GlobalFlagsSet

The global flags that control system behavior. For more information, see Gflags.exe.

### -field CriticalSectionDefaultTimeout

The critical section default time-out value.

### -field DeCommitFreeBlockThreshold

The size of the minimum block that must be freed before it is freed (de-committed), in bytes. This value is advisory.

### -field DeCommitTotalFreeThreshold

The size of the minimum total memory that must be freed in the process heap before it is freed (de-committed), in bytes. This value is advisory.

### -field LockPrefixTable

 The VA of a list of addresses where the LOCK prefix is used. These will be replaced by NOP on single-processor systems. This member is available only for x86.

### -field MaximumAllocationSize

The maximum allocation size, in bytes. This member is obsolete and is used only for debugging purposes.

### -field VirtualMemoryThreshold

The maximum block size that can be allocated from heap segments, in bytes.

### -field ProcessHeapFlags

The process heap flags. For more information, see <a href="/windows/desktop/api/heapapi/nf-heapapi-heapcreate">HeapCreate</a>.

### -field ProcessAffinityMask

The process affinity mask. For more information, see 
<a href="/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask">GetProcessAffinityMask</a>. This member is available only for .exe files.

### -field CSDVersion

The service pack version.

### -field DependentLoadFlags

### -field EditList

Reserved for use by the system.

### -field SecurityCookie

A pointer to a cookie that is used by Visual C++ or GS implementation.

### -field SEHandlerTable

 The VA of the sorted table of RVAs of each valid, unique handler in the image. This member is available only for x86.

### -field SEHandlerCount

The count of unique handlers in the table. This member is available only for x86.

### -field GuardCFCheckFunctionPointer

### -field GuardCFDispatchFunctionPointer

### -field GuardCFFunctionTable

### -field GuardCFFunctionCount

### -field GuardFlags

### -field CodeIntegrity

### -field GuardAddressTakenIatEntryTable

### -field GuardAddressTakenIatEntryCount

### -field GuardLongJumpTargetTable

### -field GuardLongJumpTargetCount

### -field DynamicValueRelocTable

### -field CHPEMetadataPointer

### -field GuardRFFailureRoutine

### -field GuardRFFailureRoutineFunctionPointer

### -field DynamicValueRelocTableOffset

### -field DynamicValueRelocTableSection

### -field Reserved2

### -field GuardRFVerifyStackPointerFunctionPointer

### -field HotPatchTableOffset

### -field Reserved3

### -field EnclaveConfigurationPointer

### -field VolatileMetadataPointer

 




#### - Reserved1

Reserved for use by the operating system.

## -remarks

If <b>_WIN64</b> is defined, then <b>IMAGE_LOAD_CONFIG_DIRECTORY</b> is defined as <b>IMAGE_LOAD_CONFIG_DIRECTORY64</b>. However, if <b>_WIN64</b> is not defined,  then <b>IMAGE_LOAD_CONFIG_DIRECTORY</b> is defined as <b>IMAGE_LOAD_CONFIG_DIRECTORY32</b>. 


```cpp
typedef struct {
    DWORD   Size;
    DWORD   TimeDateStamp;
    WORD    MajorVersion;
    WORD    MinorVersion;
    DWORD   GlobalFlagsClear;
    DWORD   GlobalFlagsSet;
    DWORD   CriticalSectionDefaultTimeout;
    DWORD   DeCommitFreeBlockThreshold;
    DWORD   DeCommitTotalFreeThreshold;
    DWORD   LockPrefixTable;            // VA
    DWORD   MaximumAllocationSize;
    DWORD   VirtualMemoryThreshold;
    DWORD   ProcessHeapFlags;
    DWORD   ProcessAffinityMask;
    WORD    CSDVersion;
    WORD    Reserved1;
    DWORD   EditList;                   // VA
    DWORD   SecurityCookie;             // VA
    DWORD   SEHandlerTable;             // VA
    DWORD   SEHandlerCount;
} IMAGE_LOAD_CONFIG_DIRECTORY32, *PIMAGE_LOAD_CONFIG_DIRECTORY32;
```

## -see-also

<a href="/windows/desktop/api/imagehlp/nf-imagehlp-getimageconfiginformation">GetImageConfigInformation</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask">GetProcessAffinityMask</a>



<a href="/windows/desktop/Debug/imagehlp-structures">ImageHlp Structures</a>



<a href="/windows/desktop/api/imagehlp/nf-imagehlp-setimageconfiginformation">SetImageConfigInformation</a>
