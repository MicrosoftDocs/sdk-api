---
UID: TP:cimfs
title: CimFS
ms.author: windowssdkdev
ms.date: 08/05/2021
ms.keywords: 
ms.service: windows
ms.subservice: windows
ms.topic: overview
ms.update-cycle: 1095-days
---

# CimFS

## -description

A [CIM](/azure/virtual-desktop/app-attach-glossary) is a file-backed image format similar in concept to a [WIM](/windows-hardware/manufacture/desktop/wim-vs-ffu-image-file-formats).

The CIM format consists of a small collection of flat files that include one or more data and metadata region files, one or more object ID files and one or more filesystem description files. As a result of their "flatness" CIMs are faster to construct, extract and delete than the equivalent raw directories they contain.

CIMs are composite in that a given image can contain multiple file system volumes which can be mounted individually while sharing the same data region backing files.

Once constructed, a CIM can be mounted with the support of the CimFS driver. The mount constructs a read-only disk and file system volume device for the image. The contents of a mounted CIM can be accessed read-only using the standard Win32 or NT API file system interface. The CimFS file system supports many of the constructs of NTFS such as security descriptors, alternate data streams, hard links, and re-parse points.

CIMs support de-duplication at the file level. If multiple copies of the same file are added to a CIM using different paths, there will only be a single copy of the file data stored in the CIM.

CIMs were originally designed and optimized to be used as a Windows Container image layout.

To develop with CimFS, you need this header:

 * [cimfs.h](../cimfs/index.md)
 
 And you will need to link with this library:
  * cimfs.lib

This [sample](https://github.com/microsoft/Windows-classic-samples/tree/main/Samples/CimFSAPI
) demonstrates how to use the Composite Image File System (CimFS) APIs to create, configure, and manipulate CimFS Images.
