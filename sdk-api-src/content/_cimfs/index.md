---
UID: TP:cimfs
title: CimFS
ms.author: windowssdkdev
ms.date: 09/09/2019
ms.keywords: 
ms.prod: windows
ms.technology: windows
ms.topic: portal
---

# CimFS

## -description

A CIM is a file-backed image format similar in concept to a WIM.

The CIM format consists of a small collection of flat files that include one or more data and metadata region files, one or more object ID files and one or more filesystem description files. As a result of their “flatness” CIMs are faster to construct, extract and delete than the equivalent raw directories they contain.

CIMs are composite in that a given image can contain multiple file system volumes which can be mounted individually while sharing the same data region backing files.

Once constructed, a CIM can be mounted with the support of the CIMFS driver. The mount constructs a read-only disk and file system volume device for the image. The contents of a mounted CIM can be accessed read-only using the standard Win32 or NT API file system interface. The CIMFS file system supports many of the constructs of NTFS such as security descriptors, alternate data streams, hard links and reparse points.

CIMs support deduplication at the file level. If multiple copies of the same file are added to a CIM using different paths, there will only be a single copy of the file data stored in the CIM.

CIMs were originally designed and optimized to be used as a Windows Container image layout.

To develop with CimFS, you need this header:

 * [cimfs.h](../cimfs/index.md)

