---
UID: NE:vswriter.VSS_RESTORE_TARGET
title: VSS_RESTORE_TARGET
author: windows-sdk-content
description: Used by a writer at restore time to indicate how all the files included in a selected component, and all the files in any component set it defines, are to be restored.
old-location: base\vss_restore_target.htm
tech.root: VSS
ms.assetid: 85b154c0-ebe8-4c17-8cab-0f886bf070e2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: VSS_RESTORE_TARGET, VSS_RESTORE_TARGET enumeration [VSS], VSS_RT_ALTERNATE, VSS_RT_DIRECTED, VSS_RT_ORIGINAL, VSS_RT_ORIGINAL_LOCATION, VSS_RT_UNDEFINED, _win32_vss_restore_target, base.vss_restore_target, enumeration [VSS], vswriter/VSS_RESTORE_TARGET, vswriter/VSS_RT_ALTERNATE, vswriter/VSS_RT_DIRECTED, vswriter/VSS_RT_ORIGINAL, vswriter/VSS_RT_ORIGINAL_LOCATION, vswriter/VSS_RT_UNDEFINED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vswriter.h
req.include-header: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsWriter.h
api_name:
 - VSS_RESTORE_TARGET
product: Windows
targetos: Windows
req.typenames: VSS_RESTORE_TARGET
req.redist: 
---

# VSS_RESTORE_TARGET enumeration


## -description


The <b>VSS_RESTORE_TARGET</b> enumeration is used 
    by a writer at restore time to indicate how all the files included in a selected component, and all the files in 
    any component set it defines, are to be restored. (See 
    <a href="https://msdn.microsoft.com/e8920cca-d944-437f-bf6a-7ce8d518746a">Working with Selectability and 
    Logical Paths</a> for information on selecting components.)

Setting a restore target modifies or overrides the restore method set during backup (see 
    <a href="https://msdn.microsoft.com/4c6be981-4271-4040-8f6e-725616355062">VSS_RESTOREMETHOD_ENUM</a>).


## -enum-fields




### -field VSS_RT_UNDEFINED

No target is defined. 
     

This value indicates an error on the part of the writer.

This value is not supported for express writers.


### -field VSS_RT_ORIGINAL

This is the default restore target. 
      

This value indicates that the restoration of the files included in a selected component (or the component set 
       defined by that component) should proceed according to the original restore method specified at backup time by 
       a <a href="https://msdn.microsoft.com/4c6be981-4271-4040-8f6e-725616355062">VSS_RESTOREMETHOD_ENUM</a> value.


### -field VSS_RT_ALTERNATE

The files are restored to a location determined from an existing alternate location mapping. 
      

The restore target should be set to <b>VSS_RT_ALTERNATE</b> only when alternate location 
       mappings have been set for all the files managed by a selected component or component set.

This value is not supported for express writers.


### -field VSS_RT_DIRECTED

Use directed targeting by the writer at restore time to restore a file.
      

Directed targeting allows a writer to control, on a file-by-file basis, how a file is 
       restored—indicating how much of a file is to be restored and into which files the 
       backed-up file is to be restored.

This value is not supported for express writers.


### -field VSS_RT_ORIGINAL_LOCATION

The files are restored to the location at which they were at backup time, even if the original 
      restore method that was specified at backup time was 
      <b>VSS_RME_RESTORE_TO_ALTERNATE_LOCATION</b>.
      

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

This value is not supported for express writers.


## -remarks



A target of <b>VSS_RT_UNDEFINED</b> indicates an error state.

At backup time, writers set the default restore behavior by indicating a restore method 
    (<a href="https://msdn.microsoft.com/4c6be981-4271-4040-8f6e-725616355062">VSS_RESTOREMETHOD_ENUM</a>) set with 
    <a href="https://msdn.microsoft.com/0e04df40-49e4-4f23-b4d5-d6b602162935">IVssCreateWriterMetadata::SetRestoreMethod</a>.

If a writer does not explicitly set the restore target of a component and any component set it defines, by 
    default it is set to <b>VSS_RT_ORIGINAL</b>.

At restore time, a <b>VSS_RESTORE_TARGET</b> value other 
    than <b>VSS_RT_ORIGINAL</b> overrides the value of the originally specified restore method 
    specified by <a href="https://msdn.microsoft.com/4c6be981-4271-4040-8f6e-725616355062">VSS_RESTOREMETHOD_ENUM</a> and set by 
    <a href="https://msdn.microsoft.com/0e04df40-49e4-4f23-b4d5-d6b602162935">IVssCreateWriterMetadata::SetRestoreMethod</a>.

Only writers (using 
    <a href="https://msdn.microsoft.com/6e8b9322-6611-4a47-aa7a-876be01d33b8">IVssComponent::SetRestoreTarget</a>) can set 
    a restore target (<b>VSS_RESTORE_TARGET</b>) and change how 
    files are restored overriding the restore method).

Requesters and writers can access the current restore target through 
    <a href="https://msdn.microsoft.com/e2361e38-8757-4a29-bbaf-7f659d1095d9">IVssComponent::GetRestoreTarget</a>.

A restore target of <b>VSS_RT_ORIGINAL</b> does not mean that files should be restored to 
    their original location, but that the originally specified restore method 
    (<a href="https://msdn.microsoft.com/4c6be981-4271-4040-8f6e-725616355062">VSS_RESTOREMETHOD_ENUM</a>) must be 
    respected. For instance, if a writer set a restore method of 
    <b>VSS_RME_RESTORE_TO_ALTERNATE_LOCATION</b> for a selected component and the restore target 
    is <b>VSS_RT_ORIGINAL</b>, files should be restored to the alternate location defined by the 
    writer.

(In this example, if a writer has failed to define alternate location mappings, then it is a writer error, and 
    the requester should report it.)

A restore target of <b>VSS_RT_ALTERNATE</b> without an alternate location mapping defined 
    constitutes a writer error, and the requester should report it as such.

See <a href="https://msdn.microsoft.com/7609c392-d5f8-48c2-8e7e-f35f56cf94f8">Non-Default Backup And Restore 
    Locations</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/e2361e38-8757-4a29-bbaf-7f659d1095d9">IVssComponent::GetRestoreTarget</a>



<a href="https://msdn.microsoft.com/6e8b9322-6611-4a47-aa7a-876be01d33b8">IVssComponent::SetRestoreTarget</a>



<a href="https://msdn.microsoft.com/4c6be981-4271-4040-8f6e-725616355062">VSS_RESTOREMETHOD_ENUM</a>
 

 

